
## 사용자 흐름

```
상품 이미지 입력
    │
    ▼
① Planning      AI가 질문하며 방향 설정
    │
    ▼
② Production    카피 · 이미지 · 레이아웃 자동 제작
    │
    ▼
③ Review        섹션별 승인 및 수정
    │
    ▼
④ Completed     최종 페이지 다운로드 · 내보내기
```

---

## 아키텍처

6개 프로젝트가 하나의 체인으로 연결됩니다.

```
P6  PageMint Client      Flutter
      │ REST + SSE
P5  PageMint Server      .NET 10 + PostgreSQL
      │ gRPC / Unix Socket
P4  OpenCode Bridge      Node.js Sidecar
      │ OpenCode SDK
P1  OpenCode             AI Engine
      │ Plugin
P2  Oh My OpenCode       Plugin Harness
      │ Plugin
P3  Design Agency        AI Personas
```

---

## AI Personas

역할이 분리된 4명의 전문가로 구성됩니다.

| | Persona | 역할 | 모델 |
|---|---|---|---|
| 🧭 | **Hermes** | 사용자 인터뷰 · 리서치 · 전체 워크플로우 조율 | GPT-5.4-nano |
| ✍️ | **Apollo** | 마케팅 카피 작성 · 스토리보드 구성 | GPT-5.4 |
| 🎨 | **Athena** | HTML/CSS 페이지 레이아웃 · 비주얼 제작 | Nano Banana |
| 🖼️ | **Pygmalion** | 이미지 생성 프롬프트 설계 · 품질 관리 | Gemini 3.1 Pro |

---

## 개발 자동화

AI 에이전트가 AI 에이전트를 개발하는 구조입니다.

**문서 규약**

| 파일 | 역할 |
|---|---|
| `CLAUDE.md` | 진입점 · 팀 에이전트 배정 |
| `AGENTS.md` | 동기화 · 이슈 스캔 · 실행 규약 |
| `ARCHITECTURE.md` | 6개 프로젝트 체인 · 공유 계약 |
| `CONTRIBUTING.md` | 언어 정책 · SOLID · DRY |
| `DESIGN_SYSTEM.md` | 색상 토큰 · 테마 · 타이포그래피 |

**QA 파이프라인**

- PR Review — Claude + Codex 이중 리뷰
- Issue Review — 이슈 자동 분석 · 코멘트
- Test Suite — 865+ 테스트 자동 실행
