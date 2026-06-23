# Copilot Studio 핸즈온 Lab — HR 채용 자동화

> **"AI에게 일을 맡기되, 결정은 사람이 내립니다."**
> Power Automate + Copilot Studio로 이력서 접수부터 면접 확정까지 HR 채용 자동화를 **직접 만들어 보는** 시티즌 개발자 대상 중급 핸즈온 과정 (약 5.5시간).

[![pages-build-deployment](https://github.com/lepela/cs_lab_v2/actions/workflows/pages.yml/badge.svg)](https://github.com/lepela/cs_lab_v2/actions/workflows/pages.yml)

🔗 **배포**: https://lepela.github.io/cs_lab_v2/

---

## 이런 분들을 위해

- Copilot Studio로 챗봇은 만들어 봤지만 **실제 업무 시스템(SharePoint·메일·승인)** 과 연결해 본 적은 없는 분
- "이건 지침으로 될까, 흐름을 만들어야 할까?" — **경계 판단**이 늘 아리송했던 분
- AI 자동화 중간에 **사람의 검토·결정을 끼워 넣는 법(HITL)** 이 궁금한 분

> 전제: Power Automate / Copilot Studio 기초를 이수했거나 흐름·에이전트·Knowledge 기본 개념을 아는 분.

## 무엇을 만드나

이력서 메일 수신 → AI 요약 적재 → 사람 승인 → 면접관 에이전트(조회·평가·질문) → 면접 확정까지, 사람과 AI가 역할을 나눠 갖는 파이프라인을 처음부터 끝까지 직접 빌드합니다.

이 과정을 관통하는 두 질문:

1. **사람은 어디에 개입하는가** — 비동기 HITL(승인) vs 대화형 HITL(확인 카드)
2. **커넥터인가, 흐름인가** — 조회·추론은 커넥터+지침으로, 상태를 바꾸는 트랜잭션은 흐름으로

## 과정 구성

| 구분 | 내용 |
|---|---|
| 오프닝 | 생태계 빅픽처 + PAD 시연 |
| 1부. 에이전트 (오전) | Lab 1 환경 받기 · Lab 2 에이전트 빚기 · Lab 3 에이전트 부리기 |
| 2부. 흐름 (오후) | Lab 4 적재 흐름 · Lab 5 승인 흐름 · Lab 6 면접 확정(흐름) · Lab 7 면접 확정(토픽) |
| 피날레 | 지원자 통계 Power BI 시연 + 경계 판단 회고 |
| 부록 | 용어집 |

---

## 로컬 실행

[Jekyll](https://jekyllrb.com/) + [Just the Docs](https://just-the-docs.com/) 테마 기반입니다.

```bash
bundle install
bundle exec jekyll serve
# http://localhost:4000/cs_lab_v2/
```

## 배포

GitHub Pages(Actions)로 배포됩니다.
- 저장소 **Settings → Pages → Source = GitHub Actions** 설정
- `main` 브랜치 push 시 `.github/workflows/pages.yml`가 빌드·배포

> ⚠️ Windows에서 `Gemfile.lock`을 만들면 리눅스 CI 빌드가 깨질 수 있습니다. `bundle lock --add-platform x86_64-linux` 후 커밋하세요(이 저장소엔 이미 적용).

---

## 상태 (작업 중)

이 교안은 **재구성 v2 진행 중**입니다.

- 본문(오프닝·Lab 1~7·피날레·부록) 초안 작성 완료
- 스크린샷은 현재 **플레이스홀더**(placehold.co) — 실제 캡처로 교체 예정
- 일부 시간·환경 세부(Lab 1 환경 배포 방식, 토픽 골격 YAML)는 빌드·계측에 맞춰 보정 중

## 데이터 고지

이 과정에 등장하는 지원자 데이터(이름·이메일·이력서)는 **모두 AI가 생성한 가상 인물**의 데이터이며, 실존 개인 정보와 무관합니다. 실습 중 실제 개인 정보를 시스템에 업로드하지 마세요.

---

*이 교안은 Claude와 협업하여 제작 중입니다.*
