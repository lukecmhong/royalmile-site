# handoff — 두 세션 분담 (2026-10-26)

Luke의 Claude 운영을 두 세션으로 나눈다. 두 세션은 서로의 대화를 보지 못하므로, 이 폴더가 둘 사이의 인수인계서다.

| 세션 | 어디서 | 맡는 일 | 읽을 파일 |
| --- | --- | --- | --- |
| 에이전트 세션 | Luke의 맥, ICD 팀 폴더에서 연 Claude Code | 기존 5명 팀(건축가·디벨로퍼·리테일 MD·마케터·디자이너)을 본체로 두고, 운영자·감사자 신설, 실시간 조사 규칙, 아침·저녁·브랜드 루틴, 노션 연동 | `agent-session.md`, `notion-contract.md` |
| 노션 세션 | claude.ai/code 클라우드 세션 (royalmile-site 저장소) | 노션 화면(대시보드)과 DB 구조 | `notion-session.md`, `notion-contract.md` |

**경계.** 직원의 행동 규칙과 수첩은 맥 폴더에 있다. 무슨 일이 있었고 무엇을 결정했는지는 노션에 있다. 두 세션이 만나는 곳은 `notion-contract.md` 의 DB 4개뿐이다. 이 계약을 바꿀 때는 이 파일을 먼저 고치고 커밋한다.

**정리 예정.** 맥 팀이 이 저장소의 `.claude/agents` · `skills` · `knowledge` · `routines` 에서 필요한 것을 옮겨 간 뒤, 저장소 쪽 사본과 클라우드 예약 3개(비활성)는 Luke 승인 후 삭제한다. 이 저장소는 원래 Royal Mile 웹사이트용이다.
