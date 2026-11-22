<div align="center">

# 🏮 안녕하세요, 박창근입니다

**조선대학교 전자공학부 지능IoT 전공** · AI 응용 프로젝트 과정

도트 마을이 있는 블로그 **Blogville**을 AI와 함께 기획하고 직접 운영하고,<br/>
팀 **심청이**에서 시각장애인용 AI 옷 코디 에이전트의 **내 옷장(RAG) · 화장 확인 · 날씨**를 맡았어요.

[![Blogville](https://img.shields.io/badge/Blogville-바로가기-ffb347?style=for-the-badge&logo=googlechrome&logoColor=white)](https://unqiuepcg.java21.net)
[![Blogville Org](https://img.shields.io/badge/Org-Blogville-1b1530?style=for-the-badge&logo=github&logoColor=white)](https://github.com/handsomeguen)
[![fashion-agent-team](https://img.shields.io/badge/Team-심청이-1e3a8a?style=for-the-badge&logo=github&logoColor=white)](https://github.com/fashion-agent-team)

</div>

## 🗂 한눈에 보기

| 프로젝트 | 소개 | 내가 한 일 | 기술 |
| --- | --- | --- | --- |
| [**🏮 Blogville**](https://github.com/handsomeguen/blogville) | 티스토리처럼 글을 쓰는 블로그에 도트 2.5D 마을과 캐릭터 성장 게임을 더한 서비스 · [사이트](https://unqiuepcg.java21.net) · [문서](https://github.com/handsomeguen/docs) | 기획, 규칙, 검증, 운영 (코드는 AI와 함께) | Next.js, TypeScript, PostgreSQL, Docker |
| [**👕 심청이 · 패션 에이전트**](https://github.com/fashion-agent-team) | 팀 프로젝트(3명) · 말로 묻고 카메라로 확인하는 시각장애인용 AI 옷 코디 에이전트 (2026.10.27 ~ 11.20) | mcp-closet, mcp-face-check(화장), mcp-weather | Spring AI(MCP), pgvector, PyTorch, ONNX |
| [**🤖 Jetson 실습**](https://github.com/AIP-1/embedding_gemma2-AIGJ_01_011) | Jetson Orin Nano에서 EmbeddingGemma 멀티모달 임베딩, 카메라 응용, 센서 시계열 예측·이상 탐지 | 실습 과제 | Python |

---

<div align="center">
  <img width="110" height="110" alt="심청이 로고" src="https://raw.githubusercontent.com/fashion-agent-team/.github/main/profile/images/simcheong-logo.png" />
  <h2>👕 심청이 · 패션 에이전트</h2>
  <p><strong>말로 묻고, 카메라로 확인하는 시각장애인용 AI 옷 코디 에이전트</strong></p>
  <p>"설명해 주는 앱은 있었지만, 골라 주는 앱은 없었습니다."</p>
  <p>📅 2026.10.27 ~ 2026.11.20 · 👥 팀 심청이(3명) · 🎤 조선대 2026 IT Festival 캡스톤디자인 경진대회 발표</p>
</div>

<p align="center"><img src="https://raw.githubusercontent.com/fashion-agent-team/.github/main/profile/images/charts/1122b-effort-hero.png" width="100%" alt="25일 동안 모델 학습 176시간 이상, 눈 화장 반복 학습 396판, 비교한 모델·방식 109가지, 머지한 PR 299개, 커밋 811개, 테스트 578개"/></p>

<table align="center">
  <tr>
    <td align="center" valign="top" width="20%"><img src="https://raw.githubusercontent.com/fashion-agent-team/.github/main/profile/images/app/1122-01-greeting.png" width="140" alt="먼저 인사"/><br/><sub>먼저 인사</sub></td>
    <td align="center" valign="top" width="20%"><img src="https://raw.githubusercontent.com/fashion-agent-team/.github/main/profile/images/app/1122-08-advice.png" width="140" alt="오늘의 추천"/><br/><sub>날씨 보고 말로 추천</sub></td>
    <td align="center" valign="top" width="20%"><img src="https://raw.githubusercontent.com/fashion-agent-team/.github/main/profile/images/app/1122-20-cam-outfit.png" width="140" alt="카메라로 옷 확인"/><br/><sub>카메라로 옷 확인</sub></td>
    <td align="center" valign="top" width="20%"><img src="https://raw.githubusercontent.com/fashion-agent-team/.github/main/profile/images/app/1122-14-closet-list.png" width="140" alt="내 옷장"/><br/><sub>내 옷장</sub></td>
    <td align="center" valign="top" width="20%"><img src="https://raw.githubusercontent.com/fashion-agent-team/.github/main/profile/images/app/1122-26-cam-face.png" width="140" alt="화장 확인"/><br/><sub>화장 확인</sub></td>
  </tr>
</table>

### 🙋 제가 맡은 부분: 내 옷장 · 화장 확인 · 날씨

| 맡은 곳 | 한 일 |
| --- | --- |
| 👚 [**mcp-closet**](https://github.com/fashion-agent-team/mcp-closet) (서버 전체) | 글 벡터(multilingual-e5) RAG 검색, 옷 사진 벡터(FashionSigLIP)로 같은 옷 합치기, 애매하면 GPT가 작은 사진 두 장으로 확인, 옷장 읽기·지우기·입은 조합 도구, 같은 옷 기준값 실측(0.60) |
| 💄 [**mcp-face-check**](https://github.com/fashion-agent-team/mcp-face-check) (화장 대칭) | 얼굴 분할 모델 비교 후 BiSeNet 선택, CelebA로 학습한 좌우 비교 모델(눈썹·입술·볼), FFHQ 실사진 기준값, 눈화장 ResNet18 앙상블(실사진 검출 70.7% → 78.6%) |
| 🌤 [**mcp-weather**](https://github.com/fashion-agent-team/mcp-weather) | 서버 구현, 연결 끊김 재시도, Open-Meteo가 안 되면 MET Norway로 넘기기 |
| 👕 **옷 종류 정확도** | mcp-clothes-state에서 글 벡터로 애매한 종류 다시 고르기, 애매할 때만 큰 모델(SigLIP2 so400m) |
| 📱 **agent · 앱** | 옷장·날씨 대화 흐름, 말투·체감 온도 바로잡기, Azure 목소리 4가지, 앱 화면 개편 "인당수의 밤"과 심청이 그림 |
| 🚀 **배포 · 문서** | 젯슨 두 대 배포 문서, 아키텍처 그림, ERD |

> 제 파트에서 모델 학습에 **109시간 이상**을 썼어요. 눈 화장 모델은 젯슨에서 **396판** 반복 학습했고, 화장 재는 방식 약 35가지, 같은 옷 찾기 사진 모델 12개, 날씨 출처 3개를 비교했어요.

| 기능 | 하는 일 |
| --- | --- |
| 🌤 **날씨·일정 맞춤 추천** | "오늘 뭐 입지?" 한마디에 날씨·일정·내 옷장을 함께 보고 말로 추천해요 |
| 📷 **카메라로 옷 확인** | 직접 학습한 모델로 옷 종류·색·무늬·얼룩·찢어짐을 찾고, 사진 찍기 버튼 없이 소리로 구도를 안내해요 |
| 💄 **얼굴 확인** | 화장이 좌우 고른지, 이 사이에 뭐가 끼지 않았는지 서버 자체 모델로만 확인해요(외부 AI로 보내지 않음) |
| 👚 **내 옷장 (RAG)** | 확인한 옷과 입은 날을 기록하고, 다음 추천 때 내 옷 중에서 골라요 |

<details>
<summary><b>🏗 아키텍처 · ERD 보기</b></summary>
<br/>
<p align="center"><img src="https://raw.githubusercontent.com/fashion-agent-team/.github/main/profile/images/architecture-v8.png" width="100%" alt="심청이 아키텍처"/></p>

- 폰 앱 → Tailscale Funnel → Nginx → gateway → agent → MCP 서버들
- **젯슨 오린 나노 8GB 두 대**에 나눠 Docker Compose로 상시 운영해요. 한 대는 gateway·agent·일정·옷장·DB, 다른 한 대는 옷 상태·얼굴·날씨 MCP와 모델 학습을 맡아요
- MCP 서버는 데이터만 돌려주고, 판단은 agent가 맡아요

<p align="center"><img src="https://raw.githubusercontent.com/fashion-agent-team/.github/main/profile/images/erd-v7.png" width="100%" alt="심청이 ERD"/></p>

- 서비스마다 스키마 하나(account · schedule · closet), 표 11개, BCNF까지 정규화

</details>

<details>
<summary><b>📈 25일 동안 남긴 흔적 보기</b></summary>
<br/>
<p align="center"><img src="https://raw.githubusercontent.com/fashion-agent-team/.github/main/profile/images/charts/1122-effort-training.png" width="100%" alt="모델 학습 시간"/></p>
<p align="center"><img src="https://raw.githubusercontent.com/fashion-agent-team/.github/main/profile/images/charts/1122-effort-daily.png" width="100%" alt="날짜별 머지 PR"/></p>

- 기능 하나도 바로 develop에 넣지 않고 **브랜치 → PR → CI 테스트 → 리뷰 → 머지**를 거쳤어요

</details>

<details>
<summary><b>📦 레포지토리 8개 보기</b></summary>
<br/>

| 레포 | 역할 |
| --- | --- |
| [fashion-agent](https://github.com/fashion-agent-team/fashion-agent) | Flutter 모바일 앱, 서비스 간 약속 문서, 배포 설정 |
| [fashion-agent-gateway](https://github.com/fashion-agent-team/fashion-agent-gateway) | API 게이트웨이, 로그인, 음성 인식·읽기 |
| [fashion-agent-agent](https://github.com/fashion-agent-team/fashion-agent-agent) | 대화와 옷 추천을 이끄는 두뇌 (Spring AI + OpenAI) |
| [mcp-weather](https://github.com/fashion-agent-team/mcp-weather) ⭐ | 오늘·날짜별 날씨 |
| [mcp-schedule](https://github.com/fashion-agent-team/mcp-schedule) | 일정, 자리·장소 종류, 아침 브리핑 |
| [mcp-clothes-state](https://github.com/fashion-agent-team/mcp-clothes-state) | 옷 종류·색·무늬·얼룩·찢어짐, 입은 모습, 색 조합 |
| [mcp-face-check](https://github.com/fashion-agent-team/mcp-face-check) ⭐ | 화장 대칭(눈썹·입술·볼·눈화장), 치아 확인 |
| [mcp-closet](https://github.com/fashion-agent-team/mcp-closet) ⭐ | 내 옷장 기록과 검색(RAG), 같은 옷 합치기 |

<sub>⭐ 제가 맡은 레포예요.</sub>

</details>

🎤 **발표 자료:** [슬라이드](https://github.com/fashion-agent-team/.github/releases/download/presentation-2026-11/simcheong-presentation.pptx) · [발표 영상](https://github.com/fashion-agent-team/.github/releases/download/presentation-2026-11/simcheong-presentation-video.mp4) · [시연 영상](https://github.com/fashion-agent-team/.github/releases/download/presentation-2026-11/simcheong-demo-video.mp4) · [팀 소개 전체 보기](https://github.com/fashion-agent-team)

---

## 🛠 기술

| 구분 | 기술 |
| :--- | :--- |
| **Web · App** | ![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white) |
| **Backend** | ![Java](https://img.shields.io/badge/Java_21-007396?style=flat-square&logo=openjdk&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white) ![Spring AI](https://img.shields.io/badge/Spring_AI_(MCP)-6DB33F?style=flat-square&logo=spring&logoColor=white) |
| **AI** | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white) ![ONNX](https://img.shields.io/badge/ONNX_Runtime-005CED?style=flat-square&logo=onnx&logoColor=white) ![FashionSigLIP](https://img.shields.io/badge/FashionSigLIP-FFD21E?style=flat-square&logo=huggingface&logoColor=black) ![BiSeNet](https://img.shields.io/badge/BiSeNet·ResNet18-EE4C2C?style=flat-square&logo=pytorch&logoColor=white) ![Jetson](https://img.shields.io/badge/Jetson_Orin-76B900?style=flat-square&logo=nvidia&logoColor=white) ![OpenAI](https://img.shields.io/badge/OpenAI_GPT-412991?style=flat-square&logo=openai&logoColor=white) |
| **Database** | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![pgvector](https://img.shields.io/badge/pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white) |
| **Infra** | ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![nginx](https://img.shields.io/badge/nginx-009639?style=flat-square&logo=nginx&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white) ![Tailscale](https://img.shields.io/badge/Tailscale-242424?style=flat-square&logo=tailscale&logoColor=white) ![Git Flow](https://img.shields.io/badge/Git_Flow-F05032?style=flat-square&logo=git&logoColor=white) |
| **Tools** | ![Claude Code](https://img.shields.io/badge/Claude_Code-D97757?style=flat-square&logo=claude&logoColor=white) |

## 🌙 요즘 하는 일

- 🏮 Blogville 운영: Git Flow, 블루-그린 무중단 배포, 배포마다 릴리스 노트
- 📚 정보처리기사 준비 중
