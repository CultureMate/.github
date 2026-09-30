<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:FF8A4C,100:EF4433&height=220&section=header&text=CultureMate&fontColor=ffffff&fontSize=64&fontAlignY=36&desc=Discover%20%C2%B7%20Understand%20%C2%B7%20Plan%20%C2%B7%20Share&descAlignY=58&descSize=18&animation=fadeIn" alt="CultureMate" width="100%" />

<img src="../assets/logo.png" alt="CultureMate logo" width="84" />

### 🎭 문화행사 발견에서 하루 코스 완성까지

서울의 문화행사를 탐색하고, **AI 소개**와 **장소 추천**을 바탕으로<br />
나만의 문화 코스를 만들고 공유하는 서비스입니다.

<br />

[![Live Demo](https://img.shields.io/badge/▶_LIVE_DEMO-FF5A3C?style=for-the-badge&logoColor=white)](https://culturemate.github.io/CultureMate-frontend/#/)
[![Project](https://img.shields.io/badge/PROJECT_OVERVIEW-24292F?style=for-the-badge&logo=github&logoColor=white)](https://github.com/CultureMate/CultureMate-platform)
[![Frontend](https://img.shields.io/badge/FRONTEND-61DAFB?style=for-the-badge&logo=react&logoColor=20232A)](https://github.com/CultureMate/CultureMate-frontend)
[![Backend](https://img.shields.io/badge/BACKEND-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)](https://github.com/CultureMate/CultureMate-backend)

<sub>데모는 별도 설치 없이 실행되며, 공개용 샘플 데이터를 사용합니다.</sub>

</div>

<br />

<table align="center">
  <tr>
    <td align="center" width="33%">
      <img src="../assets/screen-home.png" alt="CultureMate 홈" width="100%" />
      <br /><b>🏠 홈 추천</b>
      <br /><sub>HOT 행사 · 다가오는 근처 행사</sub>
    </td>
    <td align="center" width="33%">
      <img src="../assets/screen-detail.png" alt="CultureMate 행사 상세" width="100%" />
      <br /><b>📄 행사 상세</b>
      <br /><sub>AI 소개 · 주변 장소</sub>
    </td>
    <td align="center" width="33%">
      <img src="../assets/screen-events.png" alt="CultureMate 행사 목록" width="100%" />
      <br /><b>🗂️ 목록 · 코스 담기</b>
      <br /><sub>조건 검색 · 코스에 추가</sub>
    </td>
  </tr>
</table>

<br />

## 💡 Why CultureMate

> 문화행사 정보는 많지만, **무엇을 볼지 고른 뒤 어디를 함께 갈지 계획하는 과정**은 여전히 여러 서비스에 흩어져 있습니다.<br />
> CultureMate는 탐색부터 하루 동선 구성까지 **하나의 흐름**으로 연결합니다.

<div align="center">

| 🔎 01 · Discover | 🤖 02 · Understand | 📍 03 · Plan | 🔗 04 · Save & Share |
|:---:|:---:|:---:|:---:|
| **서울 문화행사 탐색** | **AI 핵심 소개 확인** | **주변·사이 장소 추천** | **코스 저장과 링크 공유** |
| 관심 분야와 일정에 맞는<br />행사 발견 | 긴 원문을<br />2~3문장으로 요약 | 행사 사이에 들를<br />장소 탐색 | 방문 순서를 정리해<br />재사용 |

**행사 발견** ➜ **AI 소개** ➜ **장소 추천** ➜ **동선 구성** ➜ **코스 공유**

</div>

<br />

## ✨ Key Features

<table>
  <tr>
    <td width="50%" valign="top">
      <h3>🎫 문화행사 탐색</h3>
      서울의 공연·전시·축제를 한곳에서 검색
      <br /><sub>🛠 서울시 문화행사 데이터 수집·정제</sub>
    </td>
    <td width="50%" valign="top">
      <h3>🤖 AI 행사 소개</h3>
      긴 행사 정보를 짧고 빠르게 이해
      <br /><sub>🛠 제한된 입력 필드, 생성 결과 저장·재사용</sub>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>📍 장소 추천</h3>
      행사 주변 또는 두 행사 사이의 장소 탐색
      <br /><sub>🛠 위치 기반 Google Places 검색</sub>
    </td>
    <td width="50%" valign="top">
      <h3>🗺️ 문화 코스</h3>
      행사와 장소를 하나의 일정으로 구성
      <br /><sub>🛠 순서 편집, 저장, 읽기 전용 공유 링크</sub>
    </td>
  </tr>
  <tr>
    <td colspan="2" valign="top">
      <h3>💛 개인화</h3>
      관심 행사와 캘린더를 다시 확인
      <br /><sub>🛠 카카오 로그인, 관심 목록, 마이페이지</sub>
    </td>
  </tr>
</table>

<br />

## 🏗️ Architecture

```mermaid
flowchart LR
    U([👤 User]) --> F[⚛️ React Web]
    F -->|REST| B[🍃 Spring Boot API]
    B --> D[(🐬 MariaDB)]
    B --> S[🏛️ 서울 열린데이터광장]
    B --> O[🤖 OpenAI]
    B --> G[📍 Google Places]
    B --> K[💬 Kakao OAuth]

    style U fill:#ffffff,stroke:#9ca3af,color:#1f2937
    style F fill:#fff1ed,stroke:#ff5a3c,color:#1f2937
    style B fill:#ecfdf5,stroke:#10b981,color:#1f2937
    style D fill:#eef2ff,stroke:#6366f1,color:#1f2937
    style S fill:#f9fafb,stroke:#d1d5db,color:#1f2937
    style O fill:#f9fafb,stroke:#d1d5db,color:#1f2937
    style G fill:#f9fafb,stroke:#d1d5db,color:#1f2937
    style K fill:#fffbeb,stroke:#f59e0b,color:#1f2937
```

## 🧰 Tech Stack

<div align="center">

| Layer | Stack |
|:---:|:---|
| **Frontend** | ![React](https://img.shields.io/badge/React_19-20232A?style=for-the-badge&logo=react&logoColor=61DAFB) ![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-0F172A?style=for-the-badge&logo=tailwindcss&logoColor=38BDF8) |
| **Backend** | ![Java](https://img.shields.io/badge/Java_17-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white) |
| **Database** | ![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white) |
| **Infra · CI** | ![Docker](https://img.shields.io/badge/Docker_Compose-2496ED?style=for-the-badge&logo=docker&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white) |
| **External API** | ![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white) ![Google Maps](https://img.shields.io/badge/Google_Places-4285F4?style=for-the-badge&logo=googlemaps&logoColor=white) ![Kakao](https://img.shields.io/badge/Kakao_OAuth-FFCD00?style=for-the-badge&logo=kakaotalk&logoColor=000000) |

</div>

<br />

## 🔧 Engineering Highlights

| | 고민 | 해결 |
|:---:|---|---|
| 🧹 | **외부 데이터 안정화** | 서울시 문화행사 원본을 서비스 모델로 정제하고 중복 데이터를 병합했습니다. |
| 💸 | **AI 비용과 응답 최적화** | 생성된 소개문을 행사별로 저장하여 같은 요청에서 재호출하지 않습니다. |
| 🧭 | **위치 기반 추천** | 행사 주변뿐 아니라 두 행사 사이의 장소까지 검색할 수 있도록 추천 흐름을 확장했습니다. |
| 🐳 | **재현 가능한 실행 환경** | 프론트엔드·백엔드·DB를 Docker Compose로 통합하고 GitHub Actions로 검증합니다. |
| 🚀 | **독립 실행 데모** | 백엔드와 API 키 없이도 주요 사용자 흐름을 확인할 수 있는 GitHub Pages 데모를 제공합니다. |

<br />

## 📦 Repositories

<div align="center">

| Repository | Role | Links |
|---|---|:---:|
| 🧩 **CultureMate-platform** | 통합 실행, 시스템 구성, 프로젝트 문서 | [![repo](https://img.shields.io/badge/Repo-24292F?style=flat-square&logo=github)](https://github.com/CultureMate/CultureMate-platform) |
| 🎨 **CultureMate-frontend** | React 기반 사용자 화면과 문화 코스 경험 | [![repo](https://img.shields.io/badge/Repo-24292F?style=flat-square&logo=github)](https://github.com/CultureMate/CultureMate-frontend) [![demo](https://img.shields.io/badge/Demo-FF5A3C?style=flat-square&logo=googlechrome&logoColor=white)](https://culturemate.github.io/CultureMate-frontend/#/) |
| ⚙️ **CultureMate-backend** | REST API, 인증, 외부 API 연동, 데이터 저장 | [![repo](https://img.shields.io/badge/Repo-24292F?style=flat-square&logo=github)](https://github.com/CultureMate/CultureMate-backend) |

</div>

<br />

## 👥 Team

<div align="center">

| Member | Role | Ownership |
|:---:|:---:|---|
| **강민구** | ![BE Lead](https://img.shields.io/badge/Backend_·_Team_Lead-6DB33F?style=flat-square) | AI 소개문, Google Places, 코스 API, 사이 장소 추천 |
| **최환우** | ![BE](https://img.shields.io/badge/Backend-6DB33F?style=flat-square) | **카카오 로그인, 서울시 API, 조회수, ERD, Docker, 통합 개선** |
| **김우석** | ![BE](https://img.shields.io/badge/Backend-6DB33F?style=flat-square) | 관심 행사, 마이페이지, 댓글, 서울시 원본 정제, 테스트 문서 |
| **문한일** | ![FE](https://img.shields.io/badge/Frontend-61DAFB?style=flat-square&logoColor=20232A) | 행사 탐색·상세, 지도, 댓글, 코스·공유 화면, UI 개선 |
| **손수연** | ![FE](https://img.shields.io/badge/Frontend-61DAFB?style=flat-square&logoColor=20232A) | 로그인, 프로필, 관심 목록, 캘린더, 마이페이지 |

</div>

<br />

<div align="center">

**🎓 LG CNS AM INSPIRE CAMP 6기 · Mini Project**

[데모 체험](https://culturemate.github.io/CultureMate-frontend/#/) · [프로젝트 문서](https://github.com/CultureMate/CultureMate-platform)

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:FF8A4C,100:EF4433&height=120&section=footer" alt="" width="100%" />

</div>
