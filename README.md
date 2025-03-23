# 우리들의 자료공유 플랫폼, XRPedia

## 1. 프로젝트 개요 (Introduction)

- **XRPedia**는 Web3, 블록체인 기반 차세대 자료 공유 플랫폼입니다. 사용자가 필요한 자료를 얻을 수 있는 사이트에서 낮은 수수료로 투명한 결제 시스템을 제공합니다. 또한 RLUSD 의 결제 방식을 통해 파일을 결제할 수 있습니다. 파일 업로드, 다운로드의 수에 따라서 포인트가 지급되며 상반기&하반기로 나누어 NFT가 발급됩니다. 이때 NFT는 point에 따라 랭킹을 매겨 주어지게 되며, 상위 3퍼, 10퍼, 40퍼 등을 통한 조건이 존재합니다.

- **XRPedia**는 어느 사용자든 쉽게 적응할 수 있는 UI/UX를 구현하여, 대중성을 높였습니다. 또한, 비교적 적은 수수료로 사용자들의 선호도를 높이며, RLUSD 결제 방식 stable한 코인으로 결제할 수 있도록 구현하였습니다.

- **Web3기술 기반 자료 공유와 보안성, 판매자와 소비자의 수익성을 접목한 플랫폼**을 경험해보세요

## 2. 문제 정의 및 해결방안 (Problem & Solution)

- **문제 1. 국내(해피캠퍼스)**
  - 지나치게 높은 수수료
  - 판매자와 구매자 사이의 신뢰성 확보 부족

- **문제 2. 해외(Course Hero)**
  - 주로 해외 대학생들 사이에서 사용중인 서비스
  - 연간 구독제 기반으로 이용
  - 한 두 개의 자료만 필요한 상황에서도 전체 구독료를 지불해야함

- **해결 방안**: Web3.0과 NFT, 자료공유를 통해 XPR와 RLUSD를 활용하여 낮은 수수료와 투명한 결제 시스템을 제공 => **Web3기반 블록체인 활용 자료 공유 플랫폼**

- **XRPedia의 강점**
  - **1) RLUSD를 이용한 거래로 수수료를 최소화**
    - 최소 수수료가 40% -> **XRPedia 10%**
    - 최대 수수료가 70% -> **XRPedia 20%**
    - **=> 최대 수수료가 70배 차이**
  - **2) NFT 혜택**
    - NFT 등급에 따른 할인 시스템
  - **3) 신뢰 랭킹 시스템**

## 3. 주요 기능 (Features)
- **1. 지갑 연동 로그인**
  - 프론트 : cognito를 활용하여 토큰을 백엔드에 넘겨주기
  - 백엔드: user 정보를 통해 지갑을 생성하는 로직

- **2. 업로드**
  - AI 중복 검증
  - 자료 임베딩(OCR 사용) 후 백터간 코사인 유사도 검사 (0.85 기준)
  - 포인트 지급
  - 자료 업로드 시 100 포인트
  - 파일 다운로드 시 10 포인트

- **3. 포인트에 따른 NFT 발급**
  - "Bronze" : 제한 없음, 혜택: 없음
  - "Silver" : 500포인트 이상인 상위 40% 유저, 혜택: 30 RLUSD, 자료 구매 시 5% RLUSD 결제, 자료 요청 수수료 5퍼 할인
  - "Gold" : 1000포인트 이상인 상위 10% 유저, 혜택: 120 RLUSD, 자료 구매 시 10% RLUSD 결제, 자료 요청 수수료 10퍼 할인
  - "Platinum" : 1500포인트 이상인 상위 3% 유저, 혜택: 400 RLUSD, 자료 구매 시 20% RLUSD 결제, 자료 요청 수수료 15% 할인
  - 상반기 & 하반기 마다 매번 갱신 -> 하나의 nft 마다 만료 기간(6개월) 이 있으며, 6개월 마다 사용자의 point와 nft가 초기화
  - 현재 시연에서는 업로드 될 때마다 NFT 발급을 하도록 하여 발급을 보여줬습니다!

- **4. 파일 결제 시스템**
  - RLUSD는 온체인 결제를 통해 사용
  - 블록체인에서 조회한 결제 내역을 기반으로 보상과 할인에 활용되는 인센티브 토큰
  - 결제 완료 시, 다운로드가 가능

## 4. 기술 스택 (Tech Stack)
- **프론트엔드** :
  - React 19, React Router v7, TypeScript,styled-components, axios,
  - MSW (Mock Service Worker), Amazon Cognito,ESLint & SWC Plugin

- **AI** :
  - Pytorch 등

- **백엔드** :
  - python, FastAPI, xrpl 등

- **인프라** :
  - AWS(API Gateway, ECS, CloudFront, Secrets Manager, SQS, S3 등), Docker

- **데이터베이스** :
  - MongoDB

- **협업 및 DevOps** :
  - Github(Github, Github Actions, Github Project), Figma, Notion, Discord

## 5. 기대효과 및 발전 가능성 (Future Improvements)
- 수수료 적음 + 투명한 거래 -> 사용자의 접근성이 좋음

## 6. 팀원 소개 (Team)
- **백엔드** :
  - 신현수 : aws 구축, 인프라 구축, AI 연동, 자료 서비스
  - 최세연 : 지갑 연동 로그인, 파일 결제
  - 임서연 : 문서 업로드, 상세 페이지, NFT 발급
  - 박문기 : 중복 검증(AI)

- **프론트** :
  - 이유진
  - 오은진
  - 김초련


## 7. 시스템 아키텍처
<img width="1427" alt="image" src="https://github.com/user-attachments/assets/50e91797-61a9-402d-b399-3e43603d5193" />
<img width="1402" alt="image" src="https://github.com/user-attachments/assets/de78e8ec-c115-45e5-8574-7912c9d3b7cb" />

