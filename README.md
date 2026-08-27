# Royal Mile — Golf & Spa Village

일본 이시카와현 고마츠, 야마시로 골프클럽 부지 내 16세대 한정 프라이빗 골프 빌리지 분양 웹사이트.

**Live** · https://rad-babka-c8a0b6.netlify.app

## Stack

프레임워크·빌드 과정 없는 순수 정적 사이트입니다.

- HTML5 + CSS(커스텀 프로퍼티 기반 디자인 토큰) + Vanilla JS
- 외부 의존성: Google Fonts(Noto Serif KR), Pretendard(jsDelivr) — 이외 없음
- 폼: Netlify Forms

## Structure

```
index.html          단일 랜딩 페이지 (마크업 · 스타일 · 스크립트 포함)
thanks.html         폼 접수 완료 페이지 (form action 대상)
netlify.toml        배포 설정 — 캐시 정책 · 보안 헤더
robots.txt
assets/img/         웹 최적화 이미지 (아래 참조)
```

## Development

```bash
python3 -m http.server 8080
# → http://localhost:8080
```

빌드 스텝이 없으므로 파일 수정 후 새로고침만 하면 됩니다.

## Deployment

Netlify가 GitHub `main` 브랜치에 연결되어 있습니다. push하면 자동 배포됩니다.

- Build command: 없음
- Publish directory: `.`
- 캐시: `assets/img/*` 1년 immutable, `*.html` no-cache (`netlify.toml`)

## Forms

문의 폼은 Netlify Forms(`data-netlify="true"`)로 동작합니다.
접수 내역: Netlify 대시보드 → Forms. 알림 설정: Site configuration → Forms → Form notifications.
honeypot 필드(`company-website`)로 스팸을 거릅니다.

## Design System

Aman 계열의 절제된 톤. 토큰은 `index.html` 상단 `:root`에 정의되어 있습니다.

| 토큰 | 값 | 용도 |
| --- | --- | --- |
| `--paper` | `#F3EEE7` | 기본 배경 |
| `--band` | `#FDFAF6` | 구분 밴드 |
| `--ink` | `#313131` | 텍스트 |
| serif | Lyon Text Web → Noto Serif KR 폴백 | 본문·제목 |
| sans | Whitney SSm → Pretendard 폴백 | 라벨·버튼·내비 |

- 본문 14px / 자간 +0.8px / weight 400 — 자간은 전부 양수, 강조색 없음
- Lyon·Whitney는 유료 서체입니다. 라이선스 구매 후 `@font-face`만 추가하면 폴백 순서에 따라 코드 수정 없이 적용됩니다.

## Images

`assets/img/`는 웹 최적화본만 포함합니다 (원본 렌더링은 저장소 외부 자산 폴더에서 관리).

- 포맷: WebP 3단 srcset (`*-640` / `*-1100` / `*-1800`) + JPEG 폴백
- 모든 `<img>`에 `width`/`height` 명시 (CLS 방지), 히어로 외 전부 `loading="lazy"`
- 갤러리 라이트박스는 `data-full` 속성의 최대 해상도 파일을 사용

## Content Notes

표기 기준 — 수정 시 해당 섹션과 푸터 고지 문구를 함께 갱신할 것.

- 세대: 68A 단독 풀빌라 15세대 · 200B 펜트하우스 1세대 (총 16세대, 토지·건물 등기 소유)
- 분양가: 68A 9억 5,000만 원(정가 10억) · 200B 18억 5,000만 원(정가 19억) — 선분양가, 2026-05 분양 기준
- 풀: 68A = 온수풀 · 200B = 온수풀 + 야외풀 (온천수 아님 — 표기 주의. 온천은 지역·빌리지 콘셉트에만 사용)
- 골프: 야마시로 36홀 · 후쿠이 국제 27홀 · 와카사 27홀 = 90홀, 기명 5인 · 연 20회 라운딩 쿠폰

## License

이미지 및 콘텐츠의 저작권은 프로젝트 시행사에 있습니다. 무단 사용을 금합니다.
