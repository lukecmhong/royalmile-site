저장소의 .claude/skills/brand-scout/SKILL.md 를 읽고 그 파이프라인을 그대로 실행한다. 오늘 요일(Asia/Seoul)에 해당하는 영역 2~3개를 대상으로 한다. 노션 브랜드 후보 DB는 collection://1af7b784-34f8-432b-9454-a547ba4ed7d3 (데이터베이스 https://app.notion.com/p/77971815a4184000812ab3659ed63b08), 프로젝트 DB는 collection://2f3644ca-b337-81ed-9e62-000bf62d92a7.

시작 전에 fetch id "memory"로 About 페이지를 읽고, .claude/knowledge/ 의 reviewer-developer.md, reviewer-operator.md, reviewer-architect.md, auditor.md 를 해당 에이전트가 읽도록 한다.

수집은 researcher 에이전트, 채점은 reviewer-developer / reviewer-operator / reviewer-architect 에이전트를 병렬로, 검수는 auditor 에이전트를 쓴다. 최종 5개를 브랜드 후보 DB에 추가한다 (상태=후보, 조회일=오늘, 출처와 공식 사이트 필수). 이미 DB에 있는 브랜드는 추가하지 않는다.

알림 본문에는 SKILL.md의 "보고" 형식(오늘의 5개, 심사위원 충돌, 다음 후보 5개, 수집 통계, 접근 실패 매체, 학습 후보)만 쓴다. 한국어. 브랜드 측 접촉, 외부 발송, 기존 DB 행 수정·삭제는 하지 않는다. 웹 접근이 전부 실패하거나 노션이 연결되지 않으면 DB에 아무것도 추가하지 말고 실패를 보고한다.

저장소(.claude/)가 세션에 없으면: 영역 14개(Tea, Dining, Wellness, Longevity, Recovery, Golf, Hospitality, Bath/Sauna, Senior Luxury, Cultural Experience, Private Club, High-end Education, Craft, Lifestyle) 중 오늘 요일 영역(월: Tea·Dining·Craft / 화: Wellness·Longevity·Recovery / 수: Golf·Hospitality / 목: Bath·Private Club·Senior Luxury / 금: Cultural·Education·Lifestyle)에서 한국 미진출 브랜드를 수집하고, 8개 기준(수요·지불의사, 운영 난이도, 초기 자본, 적합 입지, 프로젝트 결합, 복제 가능성, 지속성, 권리 확보, 각 0~3점)으로 채점해 상위 5개를 같은 방식으로 기록한다. 이 경우 보고 맨 위에 "저장소 없음, 간이 모드"라고 적는다.

끝나면 생각정리(업무일지) DB(collection://2f3644ca-b337-810a-99f2-000bd91ab6d4)에 한 건 추가한다: 이름 "브랜드 탐색 YYYY-MM-DD (영역)", 종류 일일, 날짜 오늘, 작성자 = 직원 DB의 "리테일 MD"(https://app.notion.com/p/405644cab33781d7bc00d7fef606c029), 설명 = 최종 5개 이름, 판단 필요 = 심사위원 충돌이 있으면 체크. 본문에 보고 전문.
