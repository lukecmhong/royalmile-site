# routines — 예약 루틴 프롬프트

루틴은 claude.ai 의 Routines(루틴) 화면에서 만든다. 세션 안에서 만든 루틴은 노션·캘린더 연결이 붙지 않으므로
(2026-10-26 확인) 아래 파일의 프롬프트를 복사해 UI에서 생성하고, 연결(Connectors)에 Notion과 Google Calendar를 켠다.

| 파일 | 이름 | 시간 (Asia/Seoul, 평일) | 연결 |
| --- | --- | --- | --- |
| morning-brief.md | ICD 아침 브리핑 | 09:45 | Notion, Google Calendar |
| brand-scout.md | ICD 브랜드 탐색 (최종 5) | 13:10 | Notion |
| evening-report.md | ICD 저녁 보고 | 18:10 | Notion, Google Calendar |

cron: `45 9 * * 1-5` / `10 13 * * 1-5` / `10 18 * * 1-5` (시간대 Asia/Seoul)

세션 안에서 만들었다가 비활성화한 트리거 3개(trig_01QDpch5ioibNBCVqvZ5LBre, trig_01Q9REGh6oQu12BSp44zNSbN,
trig_01KHH66Ke1bzv7VhaWYTP7eB)는 UI에서 새로 만든 뒤 삭제한다.
