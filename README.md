# BlockChainProject

## 프로젝트 팀명 : 프로젝트 작명소

### :relaxed: NamingCenter

### 리액트를 활용한 solidity 투표앱 만들기

## 프로젝트 시작일 : 2022-02-19

1. 모듈 설치
   cd client
   npm i
   truffle compile
   truffle migrate --reset

2. 서버 열기
   npm start

## 목차

[1.개요](#개요)

[2.목적](#목적)

- 기존 서비스와의 차별점

[3.전체 소스 코드](#전체-소스-코드-click)

[4.사용한 기술](#사용한-기술)

[5.주요 기능](#주요-기능)

[6.발생한 이슈 & 해결 방법](#발생한-이슈--해결-방법)

[7.상세 설명](#상세-설명)

- DB 구조 (ERD)

- 전체 흐름도

- 프로젝트 설명 PPT

[8.참여인원](#참여-인원-4명)

---

### 개요

선거 컨트랙트 작성과 Web3 사용 웹페이지 컨트랙트 연결

### 목적

> 수업시간에 배웠던 솔리디티를 직접 구현하며 내용복습
> 트러플 언박스로 기본틀 구성
> Contract 의 작동 확인 및 컴파일 여부
> Dicebear 랜덤 아바타 활용

### 사용한 기술 요약

Ethereum | Solidity
ganache
truffle
Metamask
React (클라이언트)
Web3.JS
NodeJS

### 사용 모듈 (server) :

    "@openzeppelin/contracts": "^4.5.0",
    "@truffle/hdwallet-provider": "^2.0.3",
    "@uniswap/v2-core": "^1.0.1",
    "assert": "^2.0.0",
    "bootstrap": "^5.1.3",
    "dotenv": "^16.0.0",
    "express": "^4.17.3",
    "react-bootstrap": "^2.1.2"

### 사용 모듈 (client) :

    "react": "^17.0.2",
    "react-dom": "^17.0.2",
    "react-scripts": "3.2.0",
    "web3": "^1.6.1"

### 주요 기능

- 후보자 등록
- 후보자 등록인원수 제한(5명까지)
- 투표 (계정당 투표권 1장)
- 투표결과 (당선)

## 발생한 이슈와 해결방법

다른 OS 환경에서 테스트 중 빈번한 모듈에러

> > Remix IDE에서만 컴파일 됨 (vscode 에서 확장프로그램, solc로 컴파일 불가)
> > 웹에서 컨트랙트 함수를 호출하려면 web3 객체 및 contract 가 윈두우 상에서 호출할 수 있어야함.
> > 웹에서 컨트랙트 함수를 호출 시 send 나 call로 호출해야 함
