---
title: 부록. 용어집
nav_order: 5
---

# 부록. 용어집 📚

이 과정에 등장하는 약어와 핵심 용어를 모았습니다. 본문을 읽다가 낯선 말이 나오면 이 페이지를 참고하세요.

## 약어

| 약어 | 풀네임 | 한 줄 설명 |
|---|---|---|
| <span id="abbr-sp">**SP**</span> | SharePoint | Microsoft 365의 협업·데이터 플랫폼. 이 과정에서 지원자 목록과 이력서 파일의 저장소로 사용한다 |
| <span id="abbr-hitl">**HITL**</span> | Human-in-the-Loop | AI 자동화 중간에 **사람의 검토·승인·결정**을 끼워 넣는 설계 패턴. 이 과정의 핵심 주제 |
| <span id="abbr-pad">**PAD**</span> | Power Automate Desktop | PC 화면을 직접 조작하는 데스크톱 자동화(RPA) 도구. 오프닝 시연에 등장 |
| <span id="abbr-cs">**CS**</span> | Copilot Studio | Microsoft의 에이전트(챗봇) 제작 플랫폼. 이 과정의 주 무대 |
| <span id="abbr-rag">**RAG**</span> | Retrieval-Augmented Generation | 검색 증강 생성 — 질문과 관련된 문서 조각을 찾아 AI 답변의 근거로 사용하는 기술. Knowledge가 이 방식으로 동작한다 |
| <span id="abbr-jd">**JD**</span> | Job Description | 직무기술서 — 직군별 필수·우대 요건을 정의한 문서. Knowledge 4종 중 하나 |

## 핵심 개념

| 용어 | 설명 |
|---|---|
| <span id="term-list">**목록 (List)**</span> | 행·열로 구성된 SharePoint 데이터 저장소. 지원자 한 명이 한 행(항목), 이름·이메일·전형단계 등 속성이 각 컬럼에 해당한다. 이 과정에서 모든 지원자 정보가 집결하는 **단일 진실 원천(Single Source of Truth)** 으로, 흐름과 에이전트가 공통으로 읽고 쓰는 중심 데이터다 (Lab 1) |
| <span id="term-internal-name">**내부 이름 (Internal Name)**</span> | 컬럼을 처음 만들 때 부여되는 시스템 식별자. 이후 표시 이름을 변경해도 내부 이름은 고정된다. 흐름의 동적 콘텐츠 참조나 OData 필터 쿼리가 이 이름을 사용하므로, 영문으로 생성하는 것이 권장된다 (Lab 1) |
| <span id="term-flow">**흐름 (Flow)**</span> | 트리거 → 액션 순서로 실행되는 자동화 단위. 같은 입력에 항상 같은 동작을 하는 **결정적(deterministic) 실행**이 특징이며, 상태 변경·이벤트 처리처럼 일관성이 중요한 작업에 적합하다. 이 과정에서는 적재 흐름(Lab 4)·승인 흐름(Lab 5)·면접 확정 흐름(Lab 6)이 해당된다 |
| <span id="term-connector">**커넥터 (Connector)**</span> | 에이전트나 흐름이 외부 시스템(SharePoint, Outlook 등)에 접근하는 연결 통로. 에이전트의 도구 탭에서 커넥터를 도구로 등록하면, 오케스트레이터가 사용자 질의에 따라 해당 커넥터를 자동으로 호출하고 결과를 답변 근거로 활용한다 |
| <span id="term-agent">**에이전트 (Agent)**</span> | Copilot Studio로 구성하는 AI 대화 인터페이스. 사용자의 발화를 해석해 적절한 Knowledge를 참조하거나 도구를 호출하고, 그 결과를 자연어 답변으로 생성한다. Knowledge·도구·지침을 조합해 동작하며, 이 과정의 중심 산출물이다 |
| <span id="term-knowledge">**Knowledge**</span> | 에이전트에 등록하는 참조 문서. 에이전트가 답변을 생성할 때 근거로 삼는 **"기준"** 을 담는다. 이 과정에서는 채용 가이드·직무기술서(JD)·회사 지침·평가 루브릭 4종을 사용한다. 실시간으로 변경되는 지원자 데이터(목록)와 이력서 원문(파일)은 Knowledge가 아니라 커넥터와 링크로 접근한다 (Lab 2) |
| <span id="term-corpus">**코퍼스 (Corpus)**</span> | RAG 검색 대상이 되는 문서 전체 집합. 에이전트는 질문과 관련된 조각을 이 집합 전체에서 검색한다. 이력서 수백 개를 한 코퍼스에 등록하면 "특정 지원자 한 명"만 명확하게 분리하기 어렵고 다른 지원자 내용이 혼입될 수 있다 — 이것이 이력서를 Knowledge에 등록하지 않고 링크로 1건씩 가져오는 이유다 (Lab 2·3) |
| <span id="term-instructions">**지침 (Instructions)**</span> | 에이전트의 행동 규칙을 자연어로 작성한 텍스트. 시스템 프롬프트에 해당하며, 어떤 도구를 언제 사용할지·어떤 데이터를 표시할지·무엇을 답하지 않을지 등 에이전트의 전반적인 행동 양식을 결정한다. 흐름이 코드로 분기를 정의하는 것과 달리, 지침은 자연어로 의도를 전달해 에이전트가 상황에 맞게 해석한다 |
| <span id="term-markdown">**Markdown**</span> | 특수 기호로 서식을 지정하는 경량 마크업 언어. `**굵게**`, `## 제목`, `- 목록` 처럼 사람이 읽기 쉬운 텍스트로 구조를 표현한다. Copilot Studio 지침은 Markdown으로 작성하며, `##` 헤더로 섹션을 나누고 `-` 목록으로 규칙을 열거하면 에이전트가 지침을 더 일관성 있게 따른다. → [Markdown 기본 문법](https://www.markdownguide.org/basic-syntax/) |
| <span id="term-guardrail">**가드레일 (Guardrail)**</span> | 지침으로 에이전트의 행동 범위를 좁히는 제약. "이 도구만 사용한다", "승인된 지원자만 표시한다", "데이터에 없는 내용은 생성하지 않는다"처럼, 에이전트가 의도를 벗어난 답변을 생성하는 것을 방지한다. 줄일 수 있는 모호함을 줄여 오답이 발생할 수 있는 범위 자체를 좁히는 것이 목적이다 (Lab 3·6) |
| <span id="term-topic">**토픽 (Topic)**</span> | Copilot Studio 에이전트 안에서 특정 주제·요청을 처리하는 단위 시나리오. 특정 발화 패턴이 인식되면 해당 토픽이 활성화되어 메시지·질문·조건·액션 호출 등 설정된 노드를 순서대로 실행한다. 이 과정에서는 면접 확정 HITL 흐름을 호출하는 토픽이 대표 예시다 (Lab 7) |
| <span id="term-content-approval">**콘텐츠 승인 / 승인상태**</span> | SharePoint 내장 기능. 목록 항목을 승인됨·거부됨·보류 중으로 관리한다. 직접 생성하는 컬럼이 아니라 SharePoint가 제공하는 내장 컬럼(`OData__ModerationStatus`)이며, 커넥터의 일반 항목 업데이트로는 변경할 수 없다. 승인 흐름(Lab 5)의 전용 액션이 이 값을 갱신한다 (Lab 1·5) |
| <span id="term-review-status">**전형단계**</span> | 채용 진행 단계를 기록하는 직접 생성한 Choice 컬럼(내부명 ReviewStatus). 검토중·서류합격·면접합격·최종합격·불합격 다섯 가지 값을 가진다. SharePoint 내장 승인상태와는 완전히 별개의 컬럼으로, 면접 확정(Lab 6 흐름·Lab 7 토픽)이 이 값을 변경한다 |
| <span id="term-transaction">**트랜잭션**</span> | 여러 데이터 변경이 "전부 성공 또는 전부 취소"로 묶여야 하는 작업 단위. 이 과정에서는 전형단계·AI 적합도 등 여러 컬럼을 원자적으로 갱신해야 하는 면접 확정 처리가 해당된다. 확률적으로 동작하는 에이전트가 아닌 결정적 흐름이 담당해야 하는 핵심 근거다 (Lab 6) |
| <span id="term-rubric">**평가 루브릭**</span> | 지원자 적합도를 등급으로 환산하는 채점 규칙 문서. 5개 축(R1 직군 요건·R2 경력 레벨·R3 성과·R4 협업·R5 인재상)으로 구성되며, 에이전트의 적합도 평가(C2)가 이 루브릭을 Knowledge로 참조해 등급을 산출한다. Knowledge 4종의 키스톤 역할을 한다 (Lab 2·3) |
| <span id="term-citizen-dev">**시티즌 개발자**</span> | 전문 프로그래머가 아니지만 로우코드·노코드 도구를 활용해 업무 자동화를 직접 구현하는 현업 담당자. 이 과정의 주 대상이다 |
| <span id="term-ai-builder">**AI Builder**</span> | Power Automate 안에서 제공하는 AI 기능 모음. 이 과정에서는 적재 흐름의 이력서 텍스트 추출·구조화에 사용한다 (Lab 4) |

