# The Royal Mile · Komatsu

일본 이시카와현 고마쓰, 야마시로 GC 부지 내 16세대 한정 프라이빗 골프 빌리지 분양 사이트.

정적 사이트 — 빌드 과정 없음. `index.html` 한 파일과 `assets/img/`로 구성됩니다.

## 구조

```
index.html          단일 랜딩 페이지
thanks.html         문의 접수 완료 페이지 (폼 action 대상)
netlify.toml        배포 설정 · 캐시 · 보안 헤더
assets/img/         웹 최적화된 렌더링 (webp 640/1100/1800 + jpg 폴백)
```

## 로컬 확인

```
python3 -m http.server 8080
```

## 배포

Netlify — GitHub 저장소 연결 후 push 하면 자동 배포됩니다.
- Build command: 없음 (비워둘 것)
- Publish directory: `.`

## 문의 폼

Netlify Forms(`data-netlify="true"`)를 사용합니다. 접수 내용은
Netlify 대시보드 → Forms 에서 확인하며, 알림 이메일은
Site settings → Forms → Form notifications 에서 설정합니다.

## 디자인 시스템

- 배경 `#F4F0EA` / 본문 `#2E2B27` — 강조색 없음
- 서체: Newsreader(영문 세리프) · Noto Serif KR(국문 세리프) · Pretendard(산세리프)
- 모든 제목 weight 200–300. 굵은 글씨를 쓰지 않습니다.
- 라벨은 10px 대문자, 자간 .22em

## 이미지 출처

`~/Desktop/ICD/Yamashiro GC/` 의 프로젝트 렌더링 및 라이선스 보유 스톡을
`assets/img/` 로 최적화해 반영했습니다. 원본은 이 저장소에 포함하지 않습니다.

## 표기 주의

분양가는 페이지에 노출하지 않습니다(개별 안내). 면적·세대수·일정은
VIP 브로셔(2026-05 기준) 기준이며, 변경 시 `index.html` 의 해당 섹션과
푸터 고지 문구를 함께 갱신할 것.
