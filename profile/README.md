<div align="center">

# ⛪ church-template

**교회 홈페이지를 위한 재사용 템플릿 — 프론트엔드 + 백엔드**

새 교회 추가 = 레포 복사 + `.env` 작성 + 배포.<br />
교회마다 DB와 서버를 따로 두고, 교회별 값(이름·도메인·시크릿)은 설정으로 주입합니다.

**첫 번째 사이트 → [www.eunsaem.com](https://www.eunsaem.com)** (기독교 한국침례회 은샘교회)

![Next.js](https://img.shields.io/badge/Next.js-16-000000?logo=nextdotjs)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-4.0-6DB33F?logo=springboot&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16-4169E1?logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-7-DC382D?logo=redis&logoColor=white)

</div>

<p align="center">
  <img src="https://raw.githubusercontent.com/church-template/church-frontend/main/docs/screenshots/01-home.jpg" width="49%" alt="은샘교회 홈" />
  <img src="https://raw.githubusercontent.com/church-template/church-frontend/main/docs/screenshots/02-worship.jpg" width="49%" alt="예배 시간 안내" />
</p>

## 📦 저장소

| 저장소 | 설명 |
|---|---|
| [**church-frontend**](https://github.com/church-template/church-frontend) | Next.js 웹사이트 — 교회 안내, 예배·설교, 사역, 소식(공지·일정·주보·갤러리), 성경 통독 챌린지, 차량 신청, 관리자 화면 |
| [**church-backend**](https://github.com/church-template/church-backend) | Spring Boot API 서버 — 회원·권한(RBAC), 콘텐츠, 중앙 미디어 라이브러리, 통독·차량·문의 |

## 🧭 설계 원칙

- **멀티테넌시 대신 교회마다 별도 인스턴스** — 데이터 격리를 인프라에 맡기고 코드는 한 교회 기준으로 단순하게
- **교회별 값은 설정으로** — 본문 이미지도 URL 대신 `media:{id}`로 저장해 도메인이 바뀌어도 그대로 동작
- **직분과 권한을 분리한 RBAC** — 권한 단위로 인가하고, 자기보다 낮은 역할만 부여 가능
- **고령 사용자를 고려한 단순함** — 이메일 인증·복잡한 비밀번호 정책 대신 관리자가 교인 확인

## 👤 만든 사람

<a href="https://github.com/EM-H20"><img src="https://github.com/EM-H20.png" width="48" /></a>

[홍의민 (EM-H20)](https://github.com/EM-H20) — 프론트엔드·백엔드·배포까지 1인 개발
