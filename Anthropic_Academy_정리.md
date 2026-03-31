# Anthropic Academy 완전 정리

> **원본**: https://www.anthropic.com/learn
> **정리일**: 2026-03-31
> **목적**: Anthropic이 제공하는 교육 자료를 한국어로 재구성

---

## 전체 구조 한눈에 보기

Anthropic Academy는 **3개 학습 경로**로 나뉩니다:

| 경로 | 대상 | 핵심 내용 |
|------|------|-----------|
| **Build with Claude** | 개발자 | API, SDK, 에이전트, 프롬프트 엔지니어링 등 기술 가이드 |
| **Claude for Work** | 직장인/팀 | 업무 활용법, 도구 연동, 협업, 부서별 활용 사례 |
| **Claude for You** | 개인 사용자 | AI 활용 기초, 프롬프팅 기법, AI 리터러시 과정 |

---

# 1. Build with Claude (개발자용)

API로 Claude를 활용한 앱을 만들고 싶은 개발자를 위한 경로입니다.

---

## 1-1. Claude 4 시리즈 모델

최신 모델(Sonnet 4.5, Opus 4.6)의 특징과 활용법.

| 자료 | 설명 | 링크 |
|------|------|------|
| Sonnet 4.5 신기능 | 최신 Sonnet 모델의 변경점 | [docs](https://docs.claude.com/en/docs/about-claude/models/whats-new-sonnet-4-5) |
| Claude 4 마이그레이션 | 기존 모델에서 전환하는 체크리스트 | [docs](https://docs.anthropic.com/en/docs/about-claude/models/migrating-to-claude-4) |
| 모델 선택 가이드 | 용도별 어떤 모델이 적합한지 | [docs](https://docs.anthropic.com/en/docs/about-claude/models/choosing-a-model) |
| Claude 4 프롬프팅 모범 사례 | 최적 결과를 위한 프롬프트 작성법 | [docs](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/claude-4-best-practices) |
| 모델 비교 차트 | 모델별 성능/가격 비교표 | [docs](https://docs.anthropic.com/en/docs/about-claude/models/overview) |
| 가격 안내 | Claude 4 시리즈 요금 | [docs](https://docs.anthropic.com/en/docs/about-claude/pricing) |

---

## 1-2. API & SDK

Claude를 코드에서 호출하기 위한 도구들.

### 지원 SDK (공식)
- **Python** / **TypeScript** / **Java** / **Go** / **Ruby**
- 모두 [공식 SDK 문서](https://docs.anthropic.com/en/api/client-sdks)에서 시작

### 핵심 API
| API | 설명 | 링크 |
|-----|------|------|
| Messages API | Claude와 대화하는 기본 API | [docs](https://docs.anthropic.com/en/api/messages) |
| Batch API | 여러 요청을 한꺼번에 처리 | [docs](https://docs.anthropic.com/en/docs/build-with-claude/batch-processing) |
| Prompt Caching | 반복 프롬프트 캐싱으로 비용 절감 | [docs](https://docs.anthropic.com/en/docs/build-with-claude/prompt-caching) |
| Amazon Bedrock | AWS에서 Claude 사용 | [docs](https://docs.anthropic.com/en/api/claude-on-amazon-bedrock) |
| Vertex AI | Google Cloud에서 Claude 사용 | [docs](https://docs.anthropic.com/en/api/claude-on-vertex-ai) |

### 고급 API
| API | 설명 | 링크 |
|-----|------|------|
| Admin API | 워크스페이스/권한 관리 | [docs](https://docs.anthropic.com/en/api/admin-api/) |
| Files API | 파일 업로드/관리 | [docs](https://docs.anthropic.com/en/docs/build-with-claude/files) |
| PDF 지원 | PDF 텍스트 추출 및 시각 분석 | [docs](https://docs.anthropic.com/en/docs/build-with-claude/pdf-support) |
| 프롬프트 생성 [실험적] | 좋은 프롬프트를 자동 생성 | [docs](https://docs.anthropic.com/en/api/prompt-tools-generate) |
| 프롬프트 개선 [실험적] | 기존 프롬프트를 코드에서 개선 | [docs](https://docs.anthropic.com/en/api/prompt-tools-improve) |
| 프롬프트 템플릿화 [실험적] | 변수를 자동 추출해 템플릿으로 변환 | [docs](https://docs.anthropic.com/en/api/prompt-tools-templatize) |

### 관련 강좌
| 강좌 | 링크 |
|------|------|
| Anthropic API로 빌드하기 | [skilljar](https://anthropic.skilljar.com/claude-with-the-anthropic-api) |
| Amazon Bedrock에서 Claude 사용하기 | [skilljar](https://anthropic.skilljar.com/claude-in-amazon-bedrock) |
| Google Vertex AI에서 Claude 사용하기 | [skilljar](https://anthropic.skilljar.com/claude-with-google-vertex) |

---

## 1-3. 에이전트 (Agents)

복잡한 작업을 자율적으로 이해하고, 계획하고, 실행하는 AI 에이전트 구축.

| 자료 | 설명 | 링크 |
|------|------|------|
| 에이전트 패턴 (Cookbook) | 에이전트 설계 패턴 예제 코드 | [GitHub](https://github.com/anthropics/anthropic-cookbook/tree/main/patterns/agents) |
| JSON 출력 구현 | 에이전트 제어를 위한 일관된 출력 형식 | [docs](https://docs.anthropic.com/en/docs/test-and-evaluate/strengthen-guardrails/increase-consistency) |
| MCP 소개 | 에이전트 워크플로우 개선을 위한 프로토콜 | [MCP](https://modelcontextprotocol.io/introduction) |
| 효과적인 에이전트 구축 | Anthropic 엔지니어링 블로그 (필독) | [blog](https://www.anthropic.com/engineering/building-effective-agents) |

---

## 1-4. 스킬 (Skills)

특정 작업을 더 잘 수행하도록 상세 지침을 제공하는 기능.

| 자료 | 설명 | 링크 |
|------|------|------|
| 스킬 개요 | 스킬이 뭔지 알아보기 | [docs](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview) |
| 스킬 모범 사례 | 좋은 스킬을 만드는 방법 | [docs](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/best-practices) |
| API에서 스킬 사용 | API 호출 시 스킬 적용법 | [docs](https://docs.claude.com/en/api/skills-guide) |
| Claude Code에서 스킬 사용 | CLI에서 스킬 활용법 | [docs](https://docs.claude.com/en/docs/claude-code/skills) |

---

## 1-5. MCP (Model Context Protocol)

Claude가 외부 도구/데이터에 접근할 수 있게 하는 프로토콜.

| 자료 | 설명 | 링크 |
|------|------|------|
| Claude Desktop에서 MCP 설정 | 빠른 시작 가이드 | [MCP](https://modelcontextprotocol.io/quickstart/user) |
| 공식 MCP 서버 모음 | 바로 쓸 수 있는 서버들 | [GitHub](https://github.com/modelcontextprotocol/servers) |
| Claude Code에서 MCP 사용 | CLI 환경에서 MCP 설정 | [docs](https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/tutorials#set-up-model-context-protocol-mcp) |
| 리모트 MCP 서버 | 원격 서버 연결법 | [docs](https://docs.anthropic.com/en/docs/agents-and-tools/remote-mcp-servers) |
| Messages API에서 MCP 연결 | API를 통한 MCP 서버 연동 | [docs](https://docs.anthropic.com/en/docs/agents-and-tools/mcp-connector) |
| MCP 로드맵 | 향후 개발 예정 기능 | [MCP](https://modelcontextprotocol.io/development/roadmap) |

### MCP 강좌
| 강좌 | 링크 |
|------|------|
| MCP 입문 | [skilljar](https://anthropic.skilljar.com/introduction-to-model-context-protocol) |
| MCP 심화 | [skilljar](https://anthropic.skilljar.com/model-context-protocol-advanced-topics) |

---

## 1-6. Claude Code

터미널에서 Claude를 사용하는 CLI 개발 도구.

| 자료 | 설명 | 링크 |
|------|------|------|
| 설치 가이드 | Claude Code 시작하기 | [docs](https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/overview) |
| IDE 연동 | VS Code, JetBrains 등과 통합 | [docs](https://docs.anthropic.com/en/docs/claude-code/ide-integrations) |
| 엔터프라이즈 설정 | Vertex AI, Bedrock 연결 | [docs](https://docs.anthropic.com/en/docs/claude-code/enterprise-setup) |
| 일반 워크플로우 | 자주 쓰는 작업 패턴 | [docs](https://docs.claude.com/en/docs/claude-code/common-workflows) |
| 트러블슈팅 | 문제 해결 가이드 | [docs](https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/troubleshooting) |
| 출시 영상 | YouTube 소개 영상 | [YouTube](https://www.youtube.com/watch?v=AJpK3YTTKZ4) |

### Claude Code 강좌
| 강좌 | 링크 |
|------|------|
| Claude Code 실전 | [skilljar](https://anthropic.skilljar.com/claude-code-in-action) |
| 서브에이전트 입문 | [skilljar](https://anthropic.skilljar.com/introduction-to-subagents) |
| 에이전트 스킬 입문 | [skilljar](https://anthropic.skilljar.com/introduction-to-agent-skills) |

---

## 1-7. 도구 사용 (Tool Use)

Claude에게 외부 도구/API 호출 능력을 부여하는 기능.

| 자료 | 설명 | 링크 |
|------|------|------|
| Tool Use 강좌 | 실습 코드 포함 과정 | [GitHub](https://github.com/anthropics/courses/blob/master/tool_use/README.md) |
| 데모 영상 | Tool Use 작동 예시 | [YouTube](https://www.youtube.com/watch?v=6wkFb2_cUik) |
| Cookbook 예제 | 다양한 Tool Use 시나리오 | [GitHub](https://github.com/anthropics/anthropic-cookbook/tree/main/tool_use) |
| 코드 실행 도구 | Claude가 코드를 직접 실행 | [docs](https://docs.anthropic.com/en/docs/agents-and-tools/tool-use/code-execution-tool) |
| 텍스트 에디터 도구 | 파일 편집 기능 | [docs](https://docs.anthropic.com/en/docs/agents-and-tools/tool-use/text-editor-tool) |
| 웹 검색 도구 | 실시간 웹 검색 기능 | [docs](https://docs.anthropic.com/en/docs/agents-and-tools/tool-use/web-search-tool) |

---

## 1-8. 확장 사고 (Extended Thinking)

Claude가 복잡한 문제를 단계적으로 추론하도록 하는 기능. "생각하는 시간"을 주는 것.

| 자료 | 설명 | 링크 |
|------|------|------|
| Extended Thinking 모델 소개 | 어떤 모델이 지원하는지 | [docs](https://docs.anthropic.com/en/docs/about-claude/models/extended-thinking-models) |
| Cookbook 가이드 | 코드로 구현하기 | [GitHub](https://github.com/anthropics/anthropic-cookbook/tree/main/extended_thinking) |
| 모범 사례 | 최적 결과를 위한 팁 | [docs](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/extended-thinking-tips) |
| 공식 문서 | 전체 기술 문서 | [docs](https://docs.anthropic.com/en/docs/build-with-claude/extended-thinking) |

---

## 1-9. RAG (검색 증강 생성)

외부 데이터를 검색해서 Claude의 응답을 보강하는 패턴.

> **쉽게 말하면**: Claude가 모르는 최신 정보나 사내 문서를 "검색해서 읽고 답변"하게 만드는 기법.

| 자료 | 설명 | 링크 |
|------|------|------|
| 고객 지원 에이전트 예제 | RAG 기반 CS봇 구축 | [GitHub](https://github.com/anthropics/anthropic-quickstarts/tree/main/customer-support-agent) |
| Voyage AI 임베딩 | 텍스트를 벡터로 변환 | [GitHub](https://github.com/anthropics/anthropic-cookbook/blob/main/third_party/VoyageAI/how_to_create_embeddings.md) |
| LlamaIndex 연동 | LlamaIndex 프레임워크와 통합 | [GitHub](https://github.com/anthropics/anthropic-cookbook/tree/main/third_party/LlamaIndex) |
| MongoDB RAG | MongoDB 기반 RAG 시스템 | [GitHub](https://github.com/anthropics/anthropic-cookbook/blob/main/third_party/MongoDB/rag_using_mongodb.ipynb) |
| Contextual Retrieval | 검색 품질을 높이는 기법 | [blog](https://www.anthropic.com/news/contextual-retrieval) |

---

## 1-10. 프롬프트 엔지니어링

Claude에게 좋은 지시를 내리는 기술.

| 자료 | 설명 | 링크 |
|------|------|------|
| 대화형 튜토리얼 | Jupyter 노트북으로 실습 | [GitHub](https://github.com/anthropics/courses/blob/master/prompt_engineering_interactive_tutorial/README.md) |
| 실전 시나리오 연습 | 실제 업무에 적용하는 연습 | [GitHub](https://github.com/anthropics/courses/blob/master/real_world_prompting/README.md) |
| 프롬프트 생성기 | 프롬프트 자동 생성 도구 | [docs](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/prompt-generator) |
| 전체 문서 | 프롬프트 엔지니어링 가이드 | [docs](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview) |
| 라운드테이블 영상 | 전문가 토론 영상 | [YouTube](https://www.youtube.com/watch?v=T9aRN5JkmL8) |

---

## 1-11. 평가 (Evaluations)

Claude의 성능을 체계적으로 테스트하고 개선하는 방법.

| 자료 | 설명 | 링크 |
|------|------|------|
| 강력한 평가 만들기 | 평가 설계 과정 | [GitHub](https://github.com/anthropics/courses/blob/master/prompt_evaluations/README.md) |
| 자동화된 평가 구축 | 자동 평가 파이프라인 | [GitHub](https://github.com/anthropics/anthropic-cookbook/blob/main/misc/building_evals.ipynb) |
| Eval Tool (콘솔) | 웹 콘솔에서 평가 실행 | [docs](https://docs.anthropic.com/en/docs/test-and-evaluate/eval-tool) |

---

## 1-12. 프롬프트 캐싱

자주 사용하는 프롬프트를 캐싱해서 비용과 지연 시간을 줄이는 기능.

| 자료 | 설명 | 링크 |
|------|------|------|
| 설명 영상 | 개념 소개 영상 | [YouTube](https://www.youtube.com/watch?v=h18BezoizkI) |
| Cookbook 구현 가이드 | 코드로 따라하기 | [GitHub](https://github.com/anthropics/anthropic-cookbook/blob/main/misc/prompt_caching.ipynb) |
| 공식 문서 | 전체 기술 문서 | [docs](https://docs.anthropic.com/en/docs/build-with-claude/prompt-caching) |

---

## 1-13. 비전 (Vision)

이미지를 이해하고 분석하는 Claude의 시각 능력.

| 자료 | 설명 | 링크 |
|------|------|------|
| 비전 시작하기 | 기본 사용법 | [GitHub](https://github.com/anthropics/anthropic-cookbook/blob/main/multimodal/getting_started_with_vision.ipynb) |
| 모범 사례 | 최적의 결과를 위한 팁 | [GitHub](https://github.com/anthropics/anthropic-cookbook/blob/main/multimodal/best_practices_for_vision.ipynb) |
| 이미지 텍스트 추출 | OCR 대용으로 활용 | [GitHub](https://github.com/anthropics/anthropic-cookbook/blob/main/multimodal/how_to_transcribe_text.ipynb) |
| 차트/그래프 분석 | 시각 자료 해석 | [GitHub](https://github.com/anthropics/anthropic-cookbook/blob/main/multimodal/reading_charts_graphs_powerpoints.ipynb) |

---

## 1-14. 컴퓨터 사용 (Computer Use)

Claude가 마우스와 키보드로 컴퓨터 화면을 직접 조작하는 기능.

| 자료 | 설명 | 링크 |
|------|------|------|
| 퀵스타트 데모 | 바로 체험해보기 | [GitHub](https://github.com/anthropics/anthropic-quickstarts/tree/main/computer-use-demo) |
| API 구현 가이드 | 코드로 구현하기 | [docs](https://docs.anthropic.com/en/docs/agents-and-tools/computer-use) |
| 개인정보 처리 안내 | 어떤 데이터가 처리되는지 | [privacy](https://privacy.anthropic.com/en/articles/10030352) |
| 개발 배경 | 어떻게 만들었는지 | [blog](https://www.anthropic.com/news/developing-computer-use) |

---

## 1-15. 해커톤 가이드

해커톤이나 개인 프로젝트를 빠르게 시작하기 위한 자료 모음.

| 자료 | 설명 | 링크 |
|------|------|------|
| Anthropic Console | 개발자 계정 생성 및 API 키 발급 | [console](https://console.anthropic.com) |
| 퀵스타트 가이드 | 첫 API 호출까지 | [docs](https://docs.anthropic.com/en/docs/get-started) |
| Anthropic Cookbook | 코드 예제 및 워크플로우 모음 | [GitHub](https://github.com/anthropics/anthropic-cookbook) |
| Quickstarts 저장소 | 앱 시작 템플릿 모음 | [GitHub](https://github.com/anthropics/anthropic-quickstarts) |
| 해커톤 워크숍 슬라이드 | 발표 자료 | [Google Slides](https://docs.google.com/presentation/d/1ntCqBrd7RRCu5JY6cH7-3tt-miSwNKj96B6KGjm92n0/) |

---

# 2. Claude for Work (업무 활용)

조직에서 Claude를 활용해 팀 생산성을 높이는 방법.

---

## 2-1. 처음 시작하기

| 자료 | 설명 | 링크 |
|------|------|------|
| Claude.ai 시작 가이드 | 기본 사용법 | [support](https://support.claude.com/en/articles/12997377-getting-started-with-claude-ai) |
| 활용 사례 모음 | 영감을 얻을 수 있는 예시들 | [claude.com](https://claude.com/resources/use-cases) |
| Claude 101 강좌 | 기초 과정 | [skilljar](https://anthropic.skilljar.com/claude-101) |

---

## 2-2. 최신 모델 알아보기

| 자료 | 설명 | 링크 |
|------|------|------|
| Sonnet 4.5 활용법 | Sonnet 최대 활용 팁 | [claude.com](https://claude.com/resources/tutorials/getting-the-most-out-of-sonnet-4-5-in-claude-ai) |
| Opus 4.6 활용법 | Opus 최대 활용 팁 | [claude.com](https://claude.com/resources/tutorials/get-the-most-from-claude-opus-4-6) |

---

## 2-3. 부서별 활용 사례

| 부서 | 활용 예시 | 링크 |
|------|-----------|------|
| 엔지니어링 | 코드 리뷰, 디버깅, 문서 작성 | [support](https://support.anthropic.com/en/articles/9945689-claude-for-engineering) |
| 인사(HR) | 채용 공고, 면접 질문, 정책 작성 | [support](https://support.anthropic.com/en/articles/9998942-claude-for-human-resources) |
| 마케팅 | 콘텐츠 작성, 캠페인 기획 | [support](https://support.anthropic.com/en/articles/9945697-claude-for-marketing) |
| 프로덕트 매니지먼트 | PRD 작성, 사용자 리서치 분석 | [support](https://support.anthropic.com/en/articles/9999062-claude-for-product-management) |
| 영업 | 제안서, 고객 이메일, 경쟁사 분석 | [support](https://support.anthropic.com/en/articles/9945703-claude-for-sales) |

---

## 2-4. 주요 기능

### 아티팩트 (Artifacts)
파일이나 콘텐츠를 대화 중에 생성하고 관리하는 기능.
- [아티팩트 사용법](https://support.anthropic.com/en/articles/9945615-intro-to-artifacts)

### 프로젝트 (Projects)
작업을 체계적으로 정리하고 복잡한 작업을 관리하는 기능.
- [프로젝트 사용법](https://support.anthropic.com/en/articles/9945648-intro-to-projects)

### 스킬 (Skills)
상세 지침을 저장해서 반복 작업의 품질을 높이는 기능.
- [스킬 알아보기](https://support.claude.com/en/articles/12512176-what-are-skills)
- [스킬 사용법](https://support.claude.com/en/articles/12512180-using-skills-in-claude)
- [커스텀 스킬 만들기](https://support.claude.com/en/articles/12512198-creating-custom-skills)

### 리서치 (Research)
여러 소스를 검색해 종합적인 인사이트를 제공하는 에이전틱 검색 기능.
- [리서치 시작하기](https://support.anthropic.com/en/articles/11106443-using-research)
- [Google Workspace 연동](https://support.anthropic.com/en/articles/11101545-using-research-and-google-workspace)

### 도구 연동 (Tools & Integrations)
외부 서비스를 연결해서 Claude의 능력을 확장.
- [도구 연결 가이드](https://support.anthropic.com/en/articles/11817150-connect-your-tools-to-unlock-a-smarter-more-capable-ai-companion)
- [GitHub 연동](https://support.anthropic.com/en/articles/9945670-using-the-github-integration)
- [Google Docs 연동](https://support.anthropic.com/en/articles/10389539-using-the-google-docs-integration)
- [분석 도구 사용](https://support.anthropic.com/en/articles/10227619-using-the-analysis-tool)

### Claude Cowork
실제 파일과 프로젝트에서 Claude와 함께 작업하는 기능.
- [Claude Cowork 입문 강좌](https://anthropic.skilljar.com/introduction-to-claude-cowork)

---

## 2-5. 업무용 강좌

| 강좌 | 대상 | 링크 |
|------|------|------|
| Claude 101 | 모든 사용자 | [skilljar](https://anthropic.skilljar.com/claude-101) |
| Claude Code 실전 | 개발자 | [skilljar](https://anthropic.skilljar.com/claude-code-in-action) |
| Claude Cowork 입문 | 팀 협업 | [skilljar](https://anthropic.skilljar.com/introduction-to-claude-cowork) |
| 비영리 단체용 AI 활용 | 비영리 종사자 | [skilljar](https://anthropic.skilljar.com/ai-fluency-for-nonprofits) |
| 교육자용 AI 활용 | 교사/교수 | [skilljar](https://anthropic.skilljar.com/ai-fluency-for-educators) |

---

# 3. Claude for You (개인 활용)

## AI Fluency: 프레임워크 & 기초

AI를 효과적으로, 효율적으로, 윤리적으로, 안전하게 사용하는 실무 능력을 기르는 과정.

**강좌 링크**: [AI Fluency 과정](https://anthropic.skilljar.com/ai-fluency-framework-foundations)

### 12개 레슨 구성

| # | 레슨 | 핵심 내용 |
|---|------|-----------|
| 1 | AI Fluency 소개 | 왜 AI 활용 능력이 중요한가 |
| 2 | AI Fluency 프레임워크 | 4D 프레임워크 개요 |
| 3 | 딥다이브 1: 생성형 AI란? | AI 기초 원리 이해 |
| 4 | 위임 (Delegation) | AI에게 무엇을 맡길지 판단하기 |
| 5 | 위임 적용 | 실제 상황에 위임 원칙 적용 |
| 6 | 기술 (Description) | 원하는 결과를 정확하게 표현하기 |
| 7 | 딥다이브 2: 효과적인 프롬프팅 | 프롬프트 작성 기법 심화 |
| 8 | 판별 (Discernment) | AI 결과물을 비판적으로 평가하기 |
| 9 | 기술-판별 루프 | 반복적 개선 과정 |
| 10 | 성실 (Diligence) | 책임감 있는 AI 사용 |
| 11 | 결론 | 전체 정리 |
| 12 | 추가 활동 | 실습 과제 |

> **4D 프레임워크**: Delegation(위임) → Description(기술) → Discernment(판별) → Diligence(성실)
> AI에게 뭘 맡길지 → 어떻게 지시할지 → 결과를 어떻게 평가할지 → 책임감 있게 사용하는 법

---

# 추천 학습 순서

## 비개발자 (업무 활용 목적)
1. **Claude 101** → 기본 사용법 익히기
2. **AI Fluency 과정** → AI와 효과적으로 소통하는 법
3. **부서별 활용 사례** → 내 업무에 적용
4. **아티팩트 + 프로젝트** → 고급 기능 활용

## 개발자 (앱 개발 목적)
1. **API & SDK** → Messages API로 첫 호출
2. **프롬프트 엔지니어링** → 좋은 프롬프트 작성
3. **Tool Use** → 외부 도구 연동
4. **에이전트** → 자율 에이전트 구축
5. **MCP** → 고급 도구 연결 프로토콜
6. **Claude Code** → 개발 생산성 극대화

## 민짱님 추천 (앱 개발 + Claude Code 사용자)
1. **Claude Code 실전 강좌** → 이미 사용 중이니 심화 학습
2. **프롬프트 엔지니어링** → 프롬프트 품질 향상
3. **MCP 입문 + 심화** → Claude Code에서 MCP 활용 확장
4. **에이전트 패턴** → 더 복잡한 자동화
5. **스킬** → 반복 작업 최적화
