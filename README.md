<div align="center">

# 🏮 안녕하세요, 박창근입니다

**조선대학교 전자공학부 지능IoT 전공** · AI 응용 프로젝트 과정

도트 마을이 있는 블로그 **Blogville**을 AI와 함께 기획하고 직접 운영하고,<br/>
팀 **심청이**와 시각장애인용 AI 옷 코디 에이전트를 만들었어요.

[![Blogville](https://img.shields.io/badge/Blogville-바로가기-ffb347?style=for-the-badge&logo=googlechrome&logoColor=white)](https://unqiuepcg.java21.net)
[![handsomeguen](https://img.shields.io/badge/Org-handsomeguen-1b1530?style=for-the-badge&logo=github&logoColor=white)](https://github.com/handsomeguen)
[![fashion-agent-team](https://img.shields.io/badge/Team-심청이-1e3a8a?style=for-the-badge&logo=github&logoColor=white)](https://github.com/fashion-agent-team)

</div>

## 🗂 한눈에 보기

| 프로젝트 | 소개 | 기술 |
| --- | --- | --- |
| [**🏮 Blogville**](https://github.com/handsomeguen/blogville) | 티스토리처럼 글을 쓰는 블로그에 도트 2.5D 마을과 캐릭터 성장 게임을 더한 서비스 · [사이트](https://unqiuepcg.java21.net) · [문서](https://github.com/handsomeguen/docs) | Next.js, TypeScript, PostgreSQL, Docker |
| [**👕 심청이 · 패션 에이전트**](https://github.com/fashion-agent-team) | 팀 프로젝트 · 말로 묻고 카메라로 확인하는 시각장애인용 AI 옷 코디 에이전트 (2026.10.27 ~ 11.20) | Flutter, Spring AI(MCP), YOLO, pgvector |
| [**🤖 Jetson 실습**](https://github.com/AIP-1/embedding_gemma2-AIGJ_01_011) | Jetson Orin Nano에서 EmbeddingGemma 멀티모달 임베딩, 카메라 응용, 센서 시계열 예측·이상 탐지 | Python |

---

<div align="center">
  <img width="110" height="110" alt="심청이 로고" src="https://raw.githubusercontent.com/fashion-agent-team/.github/main/profile/images/simcheong-logo.png" />
  <h2>👕 심청이 · 패션 에이전트</h2>
  <p><strong>말로 묻고, 카메라로 확인하는 시각장애인용 AI 옷 코디 에이전트</strong></p>
  <p>"설명해 주는 앱은 있었지만, 골라 주는 앱은 없었습니다."</p>
  <p>📅 2026.10.27 ~ 2026.11.20 · 👥 팀 심청이 · 🎤 조선대 2026 IT Festival 캡스톤디자인 경진대회 출품</p>
</div>

<table align="center">
  <tr>
    <td align="center"><img src="https://raw.githubusercontent.com/fashion-agent-team/.github/main/profile/images/screens/home.png" width="140" alt="심청이가 먼저 인사"/><br/><sub>심청이가 먼저 인사</sub></td>
    <td align="center"><img src="https://raw.githubusercontent.com/fashion-agent-team/.github/main/profile/images/screens/listening.png" width="140" alt="듣는 중엔 물이 다홍으로"/><br/><sub>듣는 중엔 물이 다홍으로</sub></td>
    <td align="center"><img src="https://raw.githubusercontent.com/fashion-agent-team/.github/main/profile/images/screens/advice.png" width="140" alt="날씨 보고 말로 추천"/><br/><sub>날씨 보고 말로 추천</sub></td>
    <td align="center"><img src="https://raw.githubusercontent.com/fashion-agent-team/.github/main/profile/images/screens/camera.png" width="140" alt="멈추면 알아서 찍기"/><br/><sub>멈추면 알아서 찍기</sub></td>
    <td align="center"><img src="https://raw.githubusercontent.com/fashion-agent-team/.github/main/profile/images/screens/outfit-result.png" width="140" alt="오늘의 색동"/><br/><sub>오늘의 색동</sub></td>
  </tr>
</table>

| 기능 | 하는 일 |
| --- | --- |
| 🌤 **날씨·일정 맞춤 추천** | "오늘 뭐 입지?" 한마디에 날씨·일정·내 옷장을 함께 보고 말로 추천해요. 격식 있는 일정은 드라이클리닝까지 미리 챙겨요 |
| 📷 **카메라로 옷 확인** | 직접 학습한 YOLO·색 CNN으로 옷 종류·색·무늬·얼룩·찢어짐을 찾고, 오늘 자리에 맞는지 알려 줘요. 사진 찍기 버튼 없이 소리로 구도를 안내해요 |
| 🙂 **얼굴 확인** | 화장이 좌우 고른지, 이 사이에 뭐가 끼지 않았는지 서버 자체 모델로만 확인해요(외부 AI로 보내지 않음) |
| 👚 **내 옷장 (RAG)** | 확인한 옷과 입은 날을 기록하고, FashionSigLIP 사진 벡터와 pgvector로 다음 추천 때 내 옷 중에서 골라요 |

<details>
<summary><b>🏗 아키텍처 · ERD 보기</b></summary>
<br/>
<p align="center"><img src="https://raw.githubusercontent.com/fashion-agent-team/.github/main/profile/images/architecture.png" width="100%" alt="심청이 아키텍처"/></p>

- 앱 → gateway → agent → MCP 서버 5개(날씨·일정·옷 상태·얼굴 확인·내 옷장) → PostgreSQL
- MCP 서버는 데이터만 돌려주고, 판단은 agent가 맡아요. 서버는 팀 Jetson Orin 한 대에 Docker Compose + Nginx로 운영해요

<p align="center"><img src="https://raw.githubusercontent.com/fashion-agent-team/.github/main/profile/images/erd.png" width="100%" alt="심청이 ERD"/></p>

- 서비스마다 스키마 하나(account · schedule · closet), 표 11개, BCNF까지 정규화

</details>

<details>
<summary><b>🧠 직접 학습한 모델 결과 보기</b></summary>
<br/>

| 모델 | 결과 (학습에 안 쓴 사진) |
| --- | --- |
| 얼룩·찢어짐 YOLO26n | 사진 단위 정답률 91.9%, 애매한 것만 GPT 확인 시 98.1% |
| 옷 종류 12종 YOLO26n | 내려놓은 옷 종류 86.7% (큰 분류 91.6%) |
| 옷 색 20가지 CNN | 색 계열 76.8% (예전 픽셀 규칙 45.3%) |
| 무늬 8종 YOLO26n | 정확도 88.4%, 무지/무늬 구분 91.9% |
| 화장 좌우 비교 | 눈썹 길이 비대칭 찾는 비율 22 → 84% |

</details>

<details>
<summary><b>📦 레포지토리 8개 보기</b></summary>
<br/>

| 레포 | 역할 |
| --- | --- |
| [fashion-agent](https://github.com/fashion-agent-team/fashion-agent) | Flutter 모바일 앱, 서비스 간 약속 문서, 배포 설정 |
| [fashion-agent-gateway](https://github.com/fashion-agent-team/fashion-agent-gateway) | API 게이트웨이, 로그인, 음성 읽기 (Spring Cloud Gateway) |
| [fashion-agent-agent](https://github.com/fashion-agent-team/fashion-agent-agent) | 대화와 옷 추천을 이끄는 두뇌 (Spring AI + OpenAI) |
| [mcp-weather](https://github.com/fashion-agent-team/mcp-weather) | 오늘·날짜별 날씨 |
| [mcp-schedule](https://github.com/fashion-agent-team/mcp-schedule) | 일정, 자리·장소 종류, 아침 브리핑 |
| [mcp-clothes-state](https://github.com/fashion-agent-team/mcp-clothes-state) | 옷 종류·색·무늬·얼룩·찢어짐, 색 조합 |
| [mcp-face-check](https://github.com/fashion-agent-team/mcp-face-check) | 화장 대칭, 치아 확인 |
| [mcp-closet](https://github.com/fashion-agent-team/mcp-closet) | 내 옷장 기록과 검색(RAG) |

</details>

🎤 **발표 자료:** [슬라이드](https://github.com/fashion-agent-team/.github/releases/download/presentation-2026-11/simcheong-presentation.pptx) · [발표 영상](https://github.com/fashion-agent-team/.github/releases/download/presentation-2026-11/simcheong-presentation-video.mp4) · [시연 영상](https://github.com/fashion-agent-team/.github/releases/download/presentation-2026-11/simcheong-demo-video.mp4)

---

## 🛠 기술

| 구분 | 기술 |
| :--- | :--- |
| **Web** | ![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white) ![Dart](https://img.shields.io/badge/Dart-0175C2?style=flat-square&logo=dart&logoColor=white) |
| **Backend** | ![Java](https://img.shields.io/badge/Java_21-007396?style=flat-square&logo=openjdk&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white) ![Spring AI](https://img.shields.io/badge/Spring_AI_(MCP)-6DB33F?style=flat-square&logo=spring&logoColor=white) |
| **AI** | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white) ![YOLO](https://img.shields.io/badge/YOLO26n-111F68?style=flat-square&logo=ultralytics&logoColor=white) ![ONNX](https://img.shields.io/badge/ONNX_Runtime-005CED?style=flat-square&logo=onnx&logoColor=white) ![Jetson](https://img.shields.io/badge/Jetson_Orin-76B900?style=flat-square&logo=nvidia&logoColor=white) ![OpenAI](https://img.shields.io/badge/OpenAI_GPT-412991?style=flat-square&logo=openai&logoColor=white) |
| **Database** | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![pgvector](https://img.shields.io/badge/pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white) |
| **Infra** | ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![nginx](https://img.shields.io/badge/nginx-009639?style=flat-square&logo=nginx&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white) ![Git Flow](https://img.shields.io/badge/Git_Flow-F05032?style=flat-square&logo=git&logoColor=white) |
| **Tools** | ![Claude Code](https://img.shields.io/badge/Claude_Code-D97757?style=flat-square&logo=claude&logoColor=white) |

## 🌙 요즘 하는 일

- 🏮 Blogville 운영: Git Flow, 블루-그린 무중단 배포, 배포마다 릴리스 노트
- 📚 정보처리기사 준비 중
