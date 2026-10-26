# routines — 예약 루틴 프롬프트

(2026-10-26 변경) 루틴은 **맥의 ICD 팀 폴더에서 예약 작업으로** 돌린다. 클라우드 루틴은 맥 팀의 수첩을 읽지 못하기 때문이다.
맥 Claude Code에 노션 연결을 먼저 하고, 아래 프롬프트를 맥 팀 방식에 맞게 옮긴다. 결과는 노션 팀 보고 DB에 쌓인다(`../handoff/notion-contract.md`).

| 파일 | 이름 | 시간 (Asia/Seoul, 평일) | 연결 |
| --- | --- | --- | --- |
| morning-brief.md | ICD 아침 브리핑 | 09:45 | Notion, Google Calendar |
| brand-scout.md | ICD 브랜드 탐색 (최종 5) | 13:10 | Notion |
| evening-report.md | ICD 저녁 보고 | 18:10 | Notion, Google Calendar |

cron: `45 9 * * 1-5` / `10 13 * * 1-5` / `10 18 * * 1-5` (시간대 Asia/Seoul)

클라우드에 만들었다가 비활성화한 예약 3개(trig_01QDpch5ioibNBCVqvZ5LBre, trig_01Q9REGh6oQu12BSp44zNSbN,
trig_01KHH66Ke1bzv7VhaWYTP7eB)는 맥 예약 작업이 돌기 시작하면 사용자 승인 후 삭제한다.
