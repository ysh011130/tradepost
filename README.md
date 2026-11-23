# Tradepost

게임 내 거래를 소재로 한 **거래 요청 사이트**입니다.
판매자가 아이템과 재고를 올리면, 구매자는 수량을 정해 구매 요청을 보내고, 판매자가 수락하거나 거절합니다.
실제 결제와 물건 전달은 게임 안에서 게임 화폐로 진행하며, 이 사이트는 요청과 알림만 다룹니다.

## 주요 기능

- **디스코드 로그인**: 디스코드 계정으로 로그인하고 게임 닉네임을 등록
- **판매자 승인제**: 판매 신청 → 관리자 승인 후 판매자 권한 부여
- **상품 등록**: 아이템 목록에서 선택(없으면 직접 입력), 판매 단위(낱개 또는 묶음 단위), 단위당 가격, 재고
- **구매 요청**: 수량을 정해 요청, 판매자가 수락 / 거절
- **재고 관리**: 수락 시점에 재고 차감, 거래 취소 시 복구, 동시 수락에도 재고가 음수가 되지 않도록 처리
- **알림**: 판매자는 디스코드 웹훅, 모든 알림은 사이트 알림함에도 기록

## 거래 흐름

![거래 요청 상태 흐름](docs/trade-flow.svg)

## 기술 스택

| 영역 | 기술 |
| --- | --- |
| Backend | <img src="https://img.shields.io/badge/Java_21-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java 21"/> <img src="https://img.shields.io/badge/Spring_Boot_4.1-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" alt="Spring Boot 4.1"/> <img src="https://img.shields.io/badge/Spring_Security-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white" alt="Spring Security"/> <img src="https://img.shields.io/badge/Spring_Data_JPA-6DB33F?style=for-the-badge&logo=spring&logoColor=white" alt="Spring Data JPA"/> <img src="https://img.shields.io/badge/Hibernate-59666C?style=for-the-badge&logo=hibernate&logoColor=white" alt="Hibernate"/> |
| Frontend | <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React"/> <img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white" alt="Vite"/> |
| Database | <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL"/> <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker"/> |
| Auth | <img src="https://img.shields.io/badge/Discord_OAuth2-5865F2?style=for-the-badge&logo=discord&logoColor=white" alt="Discord OAuth2"/> |
| Build | <img src="https://img.shields.io/badge/Maven-C71A36?style=for-the-badge&logo=apachemaven&logoColor=white" alt="Maven"/> |
