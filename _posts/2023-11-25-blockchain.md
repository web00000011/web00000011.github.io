---
layout: post
title: "Everything of Blockchain"
date: 2023-11-25 10:29:53
excerpt: <b>&#35;Web3.0, &#35;Blockchain, &#35;ETH, &#35;Smart Contract</b>
---
## 목차
- [블록체인이란?](#블록체인이란)
- [블록체인의 중요 기능](#블록체인의-중요-기능)
- [블록체인의 구조](#블록체인의-구조)
- [블록체인의 작동 방식](#블록체인의-작동-방식)
- [합의 알고리즘](#합의-알고리즘)
- [작업 증명 (Proof of Work, PoW)](#작업-증명-proof-of-work-pow)
- [지분 증명 (Proof of Stake, PoS)](#지분-증명-proof-of-stake-pos)
- [머클루트]()
- [이더리움이란?]()
- [이더리움 가상 머신 (EVM)]()
- [스마트 컨트랙트]()

## 블록체인이란?

![](https://www.notion.so/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F9a5130d6-cf56-4bd9-8e9b-4ac666fd88f6%2F0b9180cd-967f-4b6d-826c-82c5e3cf54bf%2FUntitled.png?table=block&id=03f24911-2b55-43d0-88f9-60ec677f99e2&spaceId=9a5130d6-cf56-4bd9-8e9b-4ac666fd88f6&width=2000&userId=54bb8d41-f1b7-45fb-8f3a-7162d9846226&cache=v)

블록체인은 쉽게 말해서 변조 방지를 위한 디지털 장부라고 볼 수 있다.  블록체인은 위와 같은 블록의 체인이며 블록 내에는 거래 내역 및 데이터들이 저장되고, 이 블록 내에 저장되는 데이터는 블록체인의 유형에 따라 다르다. 또한 이 블록체인은 중앙화로 구성되어 있는 은행과는 다르게 탈중앙화 되어 있다.

![](https://www.notion.so/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F9a5130d6-cf56-4bd9-8e9b-4ac666fd88f6%2F55476596-d523-4c54-9f9c-585048c908a2%2FUntitled.png?table=block&id=8ae0ca9f-6b6f-40c8-a81b-ffdbe97b9335&spaceId=9a5130d6-cf56-4bd9-8e9b-4ac666fd88f6&width=2000&userId=54bb8d41-f1b7-45fb-8f3a-7162d9846226&cache=v2)

중앙화의 경우에는 하나의 중앙 서버에 모든 데이터를 저장하고 있기 때문에 중앙 서버가 해킹 당하면 사용자의 데이터가 변조 되고 삭제될 수 있다. 그러나 탈중앙화의 경우 네트워크의 접속되어 있는 모든 노드가 데이터를 공유하고 있기 때문에 하나의 노드가 해킹을 당하더라도 해커는 정보를 변조하거나 삭제할 수 없다. 이것이 탈중앙화의 주 목적이다.

![](https://www.notion.so/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F9a5130d6-cf56-4bd9-8e9b-4ac666fd88f6%2F3ad2a4e7-8343-46e3-a03a-43c11d5eb77b%2FUntitled.png?table=block&id=fef43e6c-7c8d-4f2e-a703-8406c2c64975&spaceId=9a5130d6-cf56-4bd9-8e9b-4ac666fd88f6&width=2000&userId=54bb8d41-f1b7-45fb-8f3a-7162d9846226&cache=v2)

또 다른 예로는 구글의 Spreadsheet을 예로 들 수 있다. Spreadsheet을 누군가 생성을 하고, 이를 공유하면 네트워크를 통해 공유된다. 이렇게 공유된 네트워크에 사람들이 링크를 가지고 있는 누구나 접속을 해서 Spreadsheet을 읽고, 수정할 수 있다. 만약 누군가 Spreadsheet의 내용을 변경한다면 이는 이 네트워크에 접속하고 있는 모든 사용자의 컴퓨터에서 업데이트가 된다. 그러나 이때 누군가 한 명이라도 업데이트를 원치 않는다면 업데이트 되지 않는다.  블록체인도 마찬가지다. 하나의 블록이 해킹을 당해 장부의 데이터가 변조 되었다고 해도 장부를 가지고 있는 모든 사람이 동의해야 하기 때문에 변조되지 않는다.

## 블록체인의 중요 기능

1. **탈중앙화**
2. **분산 원장**
3. **불변성**
4. **합의**
5. **이중 지출의 문제 해결**

블록체인에 있어 중요한 기능을 하는 요소는 탈중앙화와 분산 원장, 불변성, 합의, 이중 지출의 문제 해결이다.

## 블록체인의 구조

![](https://www.notion.so/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F9a5130d6-cf56-4bd9-8e9b-4ac666fd88f6%2F70117f31-da8b-4bd0-bed8-4e8e92350a64%2FUntitled.png?table=block&id=33fc5068-5c1a-4da6-9793-188f601617a4&spaceId=9a5130d6-cf56-4bd9-8e9b-4ac666fd88f6&width=2000&userId=54bb8d41-f1b7-45fb-8f3a-7162d9846226&cache=v2)

일단 블록체인에서의 첫 번째로 생성되는 블록은 Genesis Block이라고 한다. Genesis Block에는 장부의 데이터가 존재하지 않는다. 

![](https://www.researchgate.net/publication/337306138/figure/fig1/AS:825909783310336@1573923645768/The-structure-of-a-Blockchain-A-block-is-composed-of-a-header-and-a-body-where-a-header.png)
그리고 두 번째 블록부터는 Index, Hash, Hash of the Previous Block, Mercle Root, Time-Stamp, Nonce로 구성되어 있는 Block-Header와 Data & Transactions로 구성되어 있는 Block-Body로 구성된다.

> Block Header

`Index`는 현재 블록체인에서의 블록의 순서를 나타내는 번호이다.

`Hash`는 블록의 고유 Hash이다. 블록체인의 모든 블록은 각 고유의 Hash를 가진다. 만약 블록을 변조하면 Hash 또한 변하게 되고 이 경우에는 해당 블록은 블록체인에 포함되지 않는다. 그러나 이 경우라도 블록은 삭제되지 않는다. 블록체인에 한 번 추가된 블록은 변경하거나 삭제할 수 없다.

`Hash of the Previous Block`은 이전 블록의 Hash이다. 모든 블록은 이전 블록의 해시를 가지고 있다. 이 때문에 블록이 변경되어 해시가 변경된 경우에 이 해시가 변경되었다고 판단할 수 있다.

`Mercle Root`는 Block-Body에 있는 Transaction의 머클 트리 루트의 해시 값으로 블록 내의 모든 Transaction을 요악한 데이터이다.

`Timestamp`는 블록이 생성된 시간이라 보면 된다.

`Nonce`는  블록 번호,  데이터, 이전 Hash와 함께 블록의 유효한 Hash를 계산하기 위한 해싱 알고리즘에 사용될 정수이다.

> Block Body

`Data & Transactions`은 거래와 관련된 정보가 저장된다. 예를 들면 보낸/받는 사람 정보, 금액과 같은 정보들이다.

```javascript
const SHA256 = require('crypto-js/sha256');
class CryptoBlock{
    constructor(index, timestamp, data, precedingHash=" "){
        this.index = index;
        this.timestamp = timestamp;
        this.data = data;
        this.previousHash = previousgHash;
        this.hash = this.computeHash();     
    }
    computeHash(){
        return SHA256(this.index + this.precedingHash + this.timestamp + JSON.stringify(this.data)).toString();
    }   
}
```
블록 생성을 위한 클래스는 위와 같이 만들 수 있다 (머클 루트는 제외 함). index는 현재 블록의 번호, timestampe는 블록이 생성되는 시간, data는 거래와 관련된 정보, previousHash에는 이전 블록의 해시, hash는 현재 블록의 해시 값이다. 그리고 현재 블록의 해시를 생성하는 메서드인 computeHash() 메서드를 보면 현재 블록의 번호, 이전 블록의 해시, 현재 블록의 생성 시간, 거래 정보를 모두 더해서 해시로 만드는 것을 확인할 수 있다.

## 블록체인의 작동 방식

![](https://www.notion.so/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F9a5130d6-cf56-4bd9-8e9b-4ac666fd88f6%2F8032fad4-dbac-4ae5-ae33-3ab957a333c2%2FUntitled.png?table=block&id=dabaabba-2b8a-4953-b24a-ab26222e96b4&spaceId=9a5130d6-cf56-4bd9-8e9b-4ac666fd88f6&width=2000&userId=54bb8d41-f1b7-45fb-8f3a-7162d9846226&cache=v2)

블록체인의 작동 방식은 먼저 사용자가 거래를 요청하면 블록이 생성되는데 이 과정에서 PoW 작업을 거쳐 특정 조건을 만족하는 유효한 블록의 해시 값을 생성하게 되고, 이때 생성된 해시가 블록의 고유 해시이다. 이후에는 브로드캐스트에 의해서 전달받은 블록은 네트워크의 모든 노드로 전달되고, 모든 노드에서  검증을 맞친 이후에 아무런 문제가 없다면 이를 블록체인에 연결한다.

```javascript
const crypto = require("crypto");
const { range } = require("lodash");
const SHA256 = (buffer) => {
    return crypto.createHash('sha256').update(buffer).digest('hex')
}

class CryptoBlock {
    constructor(index, timestamp, data, precedingHash = " ") {
        this.index = index;
        this.timestamp = timestamp;
        this.data = data;
        this.precedingHash = precedingHash;
        this.hash = this.computeHash();
        this.nonce = 0;
    }

    computeHash() {
        return SHA256(
            this.index +
            this.precedingHash +
            this.timestamp +
            JSON.stringify(this.data) +
            this.nonce
        ).toString();
    }

}

class CryptoBlockchain {
    constructor() {
        this.blockchain = [this.startGenesisBlock()];
        this.difficulty = 4;
    }
    startGenesisBlock() {
        return new CryptoBlock(0, "01/01/2020", "Init", "0");
    }

    obtainLatestBlock() {
        return this.blockchain[this.blockchain.length - 1];
    }

    addNewBlock(newBlock) {
        newBlock.precedingHash = this.obtainLatestBlock().hash;
        this.blockchain.push(newBlock);
    }

    checkChainValidity() {
        for (let i = 1; i < this.blockchain.length; i++) {
            const currentBlock = this.blockchain[i];
            const precedingBlock = this.blockchain[i - 1];

            if (currentBlock.hash !== currentBlock.computeHash()) {
                return false;
            }
            if (currentBlock.precedingHash !== precedingBlock.hash) return false;
        }
        return true;
    }
}

let smashingCoin = new CryptoBlockchain();

console.log("smashingCoin mining in progress....");

for(let i = 1; i < 4; i++){
    smashingCoin.addNewBlock(
        new CryptoBlock(i, "01/06/2020", {
            sender: "Pocas",
            recipient: "Tom",
            quantity: 50
        })
    );
}

console.log(JSON.stringify(smashingCoin, null, 4));
```
위 코드는 위에서 설명한 블록체인에 블록이 추가되기 까지의 과정을 구현한 코드이다.

![](https://www.notion.so/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F9a5130d6-cf56-4bd9-8e9b-4ac666fd88f6%2Fd3e2b848-a163-4425-beef-2f188f28a1fb%2FUntitled.png?table=block&id=69c8e87d-7ecb-4e0d-9090-9bd851d70d20&spaceId=9a5130d6-cf56-4bd9-8e9b-4ac666fd88f6&width=2000&userId=54bb8d41-f1b7-45fb-8f3a-7162d9846226&cache=v2)

그러나 코드를 실행해보면 두 번째, 세 번째 블록의 해시를 보면 합의 알고리즘이 적용되지 않은 것을 볼 수 있다. 이 경우, 블록체인 네트워크는 노드들 간에 일관된 데이터 상태를 유지하는 데 어려움을 겪을 수 있다. 합의 알고리즘은 분산된 환경에서 동일한 블록체인을 유지하기 위해 필요한 규칙과 메커니즘을 제공한다. 따라서 합의 알고리즘이 없다면 일관성 부재, 데이터 충돌과 위조, 이중 지불과 같이 보안 이슈가 발생할 수 있다.

```javascript
proofOfWork(difficulty) {
        while (
            this.hash.substring(0, difficulty) !== Array(difficulty + 1).join("0")
        ) {
            this.nonce++;
            this.hash = this.computeHash();
        }
    }
```
위와 같은 함수를 추가하고 다시 코드를 실행 해보자.

![](https://www.notion.so/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F9a5130d6-cf56-4bd9-8e9b-4ac666fd88f6%2Fcf170b36-4270-4554-98c1-152d43d37653%2FUntitled.png?table=block&id=d2864ce8-20ec-4af4-87a9-dbe40f96a61e&spaceId=9a5130d6-cf56-4bd9-8e9b-4ac666fd88f6&width=2000&userId=54bb8d41-f1b7-45fb-8f3a-7162d9846226&cache=v2)

블록의 해시를 보면 0이 4개로 시작하는 것을 볼 수 있다. 즉 nonce 값을 이용해서 해시를 만드는데 만약  difficulty(난이도)와 충족되는 해시가 아니라면 nonce의 값을 증가 시켜서 충족되는 해시가 나올 때 까지 루프를 타게 된다.

위 코드는 따로 난이도 조절은  없고, 예시로 든 코드이지만 실제로 블록체인 네트워크는 일정한 간격으로 새로운 블록을 생성하는 것을 목표로 하고 있기 때문에 난이도 조절을 한다.

## 합의 알고리즘

합의 알고리즘은 단일 노드나 노드 그룹이  네트워크를 조작할 수 없도록 하여 블록체인의 무결성을 유지하는 역할을 한다. 쉽게 말해 이는 블록체인 네트워크에 합의를 달성하는 기술이라고 볼 수 있다.

## 작업 증명 (Proof of Work, PoW)

블록체인의 합의 알고리즘 중 하나인 작업 증명은 특정한 작업을 통해 무언가 증명한다라는 의미를 가지고 있다. 이 과정에서 해시가 생성되는데 해시를 생성하기 전에 특정한 작업을 통해 조건에 맞는 논스 값을 찾는다. 이때 논스 값을 찾을 때 난이도라는 것이 있는데 난이도에 따라서 논스 값을 찾는 시간이 오래 걸릴 수도 있고, 적게 걸릴 수도 있다.

```plaintext
A : Block 0000f67ff4f28c53dc1a53d0cc5a18cc469d0266293df522f772c95b9a053a08
B : Block 00000003cc073bd06073fa9a10aa2fc6dbcb1451ce11e57aa059957612c1ab71
```
A 블록의 앞 부분을 보면 0이 4개 B 블록의 앞 부분을 보면 0이 6개가 있는 것을 볼 수 있다. 이것이 난이도이다. 난이도가 늘어날 수록 해시 앞 부분이 0 * 난이도의 수와 일치하는 해시의 논스 값을 찾아야 한다. 

```plaintext
Bitcoin Block
818,405 : 00000000000000000003dfee45ec31f096acca2a933df216bd373b800dac11dd

Bitcoin Block
818,403 : 00000000000000000004be497352098e30b362433f37d07140bcaa8454020b58
0000000000000000000379e25d3695e0ae78e6e7c95c6f1afd676ed20fc7ac94
```
위의 해시는 최신 비트코인 블록의 해시 값이다. 

```plaintext
CryptoBlock {
  index: 1,
  timestamp: 1700909310,
  data: { sender: 'Pocas', recipient: 'Tom', quantity: 50 },
  precedingHash: '6b8467d6436d83fd1e22e9660d90ef8b35792dacfa75a1d08406d3ebdc08cbc4',
  hash: '721c2426199b3527ea4b000a4d0e27374b6dc11cdae4c2415b2a37721c8f55a9',
  difficulty: 0,
  nonce: 0
}
CryptoBlock {
  index: 2,
  timestamp: 1700909310,
  data: { sender: 'Pocas', recipient: 'Tom', quantity: 50 },
  precedingHash: '721c2426199b3527ea4b000a4d0e27374b6dc11cdae4c2415b2a37721c8f55a9',
  hash: '0d2733eb1bfe02921da7abc60e5f1f756985a5934aac43bd762aed3bcb17296f',
  difficulty: 0,
  nonce: 0
}
CryptoBlock {
  index: 3,
  timestamp: 1700909310,
  data: { sender: 'Pocas', recipient: 'Tom', quantity: 50 },
  precedingHash: '0d2733eb1bfe02921da7abc60e5f1f756985a5934aac43bd762aed3bcb17296f',
  hash: 'fd169f49e3313a6a3ed0daed78ea4b242af8025182a609f8689717c5f1be7646',
  difficulty: 0,
  nonce: 0
}
CryptoBlock {
  index: 4,
  timestamp: 1700909310,
  data: { sender: 'Pocas', recipient: 'Tom', quantity: 50 },
  precedingHash: 'fd169f49e3313a6a3ed0daed78ea4b242af8025182a609f8689717c5f1be7646',
  hash: '689c8bcefaad4320ff7ffee387de834479f4605ffef3ce739f2ce7afbb7958d0',
  difficulty: 0,
  nonce: 0
}
CryptoBlock {
  index: 5,
  timestamp: 1700909310,
  data: { sender: 'Pocas', recipient: 'Tom', quantity: 50 },
  precedingHash: '689c8bcefaad4320ff7ffee387de834479f4605ffef3ce739f2ce7afbb7958d0',
  hash: 'dcc7ef1c10eff0d20da8cdc5642de7b4b914aba8690d0eb22ecbc58535dd91e3',
  difficulty: 0,
  nonce: 0
}
CryptoBlock {
  index: 6,
  timestamp: 1700909310,
  data: { sender: 'Pocas', recipient: 'Tom', quantity: 50 },
  precedingHash: 'dcc7ef1c10eff0d20da8cdc5642de7b4b914aba8690d0eb22ecbc58535dd91e3',
  hash: 'd5ad47ba4d90c23cb055aeeb785d27cf4910e1dc6008e9230987d514d9a52786',
  difficulty: 0,
  nonce: 0
}
CryptoBlock {
  index: 7,
  timestamp: 1700909310,
  data: { sender: 'Pocas', recipient: 'Tom', quantity: 50 },
  precedingHash: 'd5ad47ba4d90c23cb055aeeb785d27cf4910e1dc6008e9230987d514d9a52786',
  hash: '733a5bef6f8430bf55efaab6a25cabd2d1e3b13a083f630f9c7f062325bbfc4e',
  difficulty: 0,
  nonce: 0
}
CryptoBlock {
  index: 8,
  timestamp: 1700909310,
  data: { sender: 'Pocas', recipient: 'Tom', quantity: 50 },
  precedingHash: '733a5bef6f8430bf55efaab6a25cabd2d1e3b13a083f630f9c7f062325bbfc4e',
  hash: '0885eed98f9582156424ec2e4c826c0c0119d1d5e5ce035cb221cbc53025bcff',
  difficulty: 0,
  nonce: 0
}
CryptoBlock {
  index: 9,
  timestamp: 1700909310,
  data: { sender: 'Pocas', recipient: 'Tom', quantity: 50 },
  precedingHash: '0885eed98f9582156424ec2e4c826c0c0119d1d5e5ce035cb221cbc53025bcff',
  hash: '3681b23f553ec6dd56e65ee4131250b0d589e4a648975a6034f514c321e6fbd8',
  difficulty: 0,
  nonce: 0
}
CryptoBlock {
  index: 10,
  timestamp: 1700909310,
  data: { sender: 'Pocas', recipient: 'Tom', quantity: 50 },
  precedingHash: '3681b23f553ec6dd56e65ee4131250b0d589e4a648975a6034f514c321e6fbd8',
  hash: '1bfacdf37afd8e72a8b8edb6941bd3b0974cb1291e2c388a71415ca9b55ec4ca',
  difficulty: 0,
  nonce: 0
}
1
CryptoBlock {
  index: 11,
  timestamp: 1700909310,
  data: { sender: 'Pocas', recipient: 'Tom', quantity: 50 },
  precedingHash: '1bfacdf37afd8e72a8b8edb6941bd3b0974cb1291e2c388a71415ca9b55ec4ca',
  hash: '04da5d9eba6af3ef0285fe3564a901bf1e44aab332a2e95ede22f92b2d997042',
  difficulty: 1,
  nonce: 2
}
CryptoBlock {
  index: 12,
  timestamp: 1700909310,
  data: { sender: 'Pocas', recipient: 'Tom', quantity: 50 },
  precedingHash: '04da5d9eba6af3ef0285fe3564a901bf1e44aab332a2e95ede22f92b2d997042',
  hash: '0924f09d6f6ffaeba0e14a71094916576a07883bc734c4ac95e0f54ad27d62e2',
  difficulty: 1,
  nonce: 3
}
```
위는 예산 채굴 시간과 난이도 조절 수를 각 10으로 설정한 후 PoS를 해서 블록을 생성한 결과이다. 블록의 난이도를 보면 10번째까지는 난이도가 0이였다가 10 이후부터는 난이도가 올라간 것을 볼 수 있다.

```
CryptoBlock {
  index: 69,
  timestamp: 1700909400,
  data: { sender: 'Pocas', recipient: 'Tom', quantity: 50 },
  precedingHash: '00000054e898e4cddd4d4d0e836b4cc270d3016d3194531ccb1f1f82c1202610',
  hash: '0000000f7449f9c543756aa037d21bc3d828d3986da022217fbded98276785ea',
  difficulty: 6,
  nonce: 7487662
}
CryptoBlock {
  index: 70,
  timestamp: 1700909409,
  data: { sender: 'Pocas', recipient: 'Tom', quantity: 50 },
  precedingHash: '0000000f7449f9c543756aa037d21bc3d828d3986da022217fbded98276785ea',
  hash: '00000005456f6faceed5d54926425ea07aa2e6cfe7556b8de115f129817568db',
  difficulty: 6,
  nonce: 34368702
}
CryptoBlock {
  index: 71,
  timestamp: 1700909449,
  data: { sender: 'Pocas', recipient: 'Tom', quantity: 50 },
  precedingHash: '00000005456f6faceed5d54926425ea07aa2e6cfe7556b8de115f129817568db',
  hash: '00000003cc073bd06073fa9a10aa2fc6dbcb1451ce11e57aa059957612c1ab71',
  difficulty: 7,
  nonce: 88725539
}
```
이후 69, 70, 71 블록을 보면 난이도가 생성하여 논스 값을 최대 88725539번을 돌려서 찾은 것을 확인할 수 있다. 이처럼 난이도가 올라가면 조건의 맞는 논스 값을 찾는데 오래 걸린다.

## 지분 증명 (Proof of Stake, PoS)

Write when I want