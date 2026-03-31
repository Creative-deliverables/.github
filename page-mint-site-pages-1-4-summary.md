# PageMint 사이트 1~4페이지 정리

기준 링크
- 사이트: https://cyberprophet.github.io/page-mint/
- 저장소: https://github.com/Creative-deliverables/page-mint-creation-platform

참고
- 이 사이트는 여러 라우트로 나뉜 일반 웹사이트라기보다, **슬라이드형 단일 HTML**에 가까운 구조로 보입니다.
- 따라서 아래 정리는 공개 페이지의 **표시 순서상 1~4번째 섹션(슬라이드)** 을 기준으로 재구성한 것입니다.

---

## 1페이지 — 페이지민트 소개와 사용자 경험 흐름

### 핵심 메시지
- 페이지민트는 **상품 상세페이지 제작을 AI 에이전트 팀이 대신하는 서비스**로 소개됩니다.
- 한 장의 상품 이미지와 짧은 설명에서 시작해, 최종 상세페이지 제작까지 이어지는 전체 사용자 흐름을 전면에 배치합니다.

### 사용자 플로우
1. **Planning**
   - 상품 이미지와 간단한 설명 입력
   - AI가 질문을 던지며 방향 설정
2. **Production**
   - 카피, 이미지, 레이아웃 자동 제작
3. **Review**
   - 섹션별 리뷰
   - 승인 및 수정
4. **Completed**
   - 최종 페이지 출력
   - 다운로드 및 내보내기

### 해석
- 첫 페이지는 제품 소개보다 먼저 **사용자가 어떤 결과를 얻게 되는지**를 보여줍니다.
- 즉, 기술 설명보다 **완성 흐름과 UX 가치**를 앞세운 구조입니다.

---

## 2페이지 — PageMint의 시스템 구조

### 핵심 메시지
- 사용자의 요청 하나가 **6개 프로젝트 체인**을 거쳐 처리된다고 설명합니다.
- 프론트엔드, 서버, 브리지, AI 엔진, 플러그인 하네스, 페르소나 레이어가 연결된 구조를 강조합니다.

### 구조 요약
- **Project 6: PageMint Client (Flutter)**
- **Project 5: PageMint Server (.NET 10)**
- **PostgreSQL**
- **Project 4: Bridge (Node.js Sidecar)**
- **Project 1: AI Engine (OpenCode)**
- **Project 2: Oh My Plugin Harness**
- **Project 3: Design Agency AI Personas**

### 연결 방식
- Client ↔ Server: **REST + SSE**
- Server ↔ Bridge: **gRPC / Unix Socket**
- Bridge ↔ AI/Plugin Layer: **OpenCode SDK / Plugin 기반 연결**

### 해석
- 이 페이지는 “단순한 생성 툴”이 아니라, **다중 프로젝트로 분리된 생성 플랫폼**이라는 점을 보여줍니다.
- 기술적 신뢰성과 확장성을 전달하려는 의도가 강합니다.

---

## 3페이지 — Project 3: AI Personas 소개

### 핵심 메시지
- PageMint는 하나의 모델이 전부를 처리하는 방식이 아니라, **역할별로 분리된 4명의 AI 전문가**가 협업하는 구조라고 설명합니다.

### 4개 페르소나
- **Hermes — Director**
  - 사용자 인터뷰
  - 리서치
  - 전체 워크플로우 조율
- **Apollo — Copywriter**
  - 마케팅 카피 작성
  - 스토리보드 구성
- **Athena — Designer**
  - HTML/CSS 페이지 제작
  - 레이아웃과 비주얼 구성
- **Pygmalion — Image Engineer**
  - 이미지 생성 프롬프트 설계
  - 품질 관리

### 표시된 모델 매핑
- Hermes: **GPT-5.4-nano**
- Apollo: **GPT-5.4**
- Athena: **Nano Banana**
- Pygmalion: **Gemini 3.1 Pro**

### 해석
- 이 페이지는 PageMint의 차별점을 **멀티 에이전트 협업 구조**로 설명합니다.
- 특히 기획, 카피, 디자인, 이미지 엔지니어링을 분리함으로써 **품질 책임이 역할별로 나뉜다**는 점을 강조합니다.

---

## 4페이지 — 개발도 AI와 함께

### 핵심 메시지
- PageMint는 단지 AI로 결과물을 만드는 서비스가 아니라, **AI 에이전트가 AI 에이전트를 개발하는 구조**까지 포함한다고 설명합니다.

### 소개되는 개발/운영 요소
- 문서와 규약 중심 운영
  - `CLAUDE.md`
  - `AGENTS.md`
  - `ARCHITECTURE.md`
  - `CONTRIBUTING.md`
  - `DESIGN_SYSTEM.md`
  - `deployment.md`
  - `pr-workflow.md`
- 메타 프로젝트, 디자인 에이전시, 브리지, 서버, 클라이언트가 각각 역할 분담
- QA 항목으로
  - **PR Review Claude + Codex 이중 리뷰**
  - **Issue Review 자동 분석·코멘트**
  - **865+ 테스트 자동 실행**

### 해석
- 이 페이지의 초점은 “우리도 AI로 개발한다”가 아니라,
  **개발 프로세스 자체가 자동화되고 체계화되어 있다**는 점에 있습니다.
- 즉, 제품뿐 아니라 **개발 운영 방식 자체도 PageMint의 경쟁력**이라는 메시지입니다.

---

## 1~4페이지를 한 줄로 요약하면

- **1페이지:** 사용자 관점의 제작 흐름 제시
- **2페이지:** 6개 프로젝트로 이어지는 시스템 아키텍처 설명
- **3페이지:** 역할 분리된 4명의 AI 페르소나 소개
- **4페이지:** AI 기반 개발 운영과 QA 체계 강조

## 전체 인상

첫 4페이지는 아래 순서로 설계되어 있습니다.
1. **무엇을 해결하는가**
2. **어떻게 돌아가는가**
3. **누가 역할을 맡는가**
4. **어떻게 개발·검증되는가**

즉, 소개 → 구조 → 역할 → 운영으로 이어지는 피치/아키텍처 하이브리드형 구성입니다.
