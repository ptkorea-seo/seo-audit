# SEO Audit Dashboard

Screaming Frog 엑셀 파일을 업로드하거나 URL을 입력해 Title 길이 · H1 유무를 점수화하는 경량 SEO 분석 도구입니다.

## 사용 방법

### 엑셀 분석 (Screaming Frog)
1. Screaming Frog에서 **Internal HTML** 리포트를 `.xlsx`로 내보냅니다.
2. 파일을 업로드하고 **분석하기** 버튼을 클릭합니다.
3. URL 필터를 입력하면 특정 페이지만 분석할 수 있습니다.

### URL 단독 분석
엑셀 없이 URL만 입력하면 해당 페이지의 Title · Description 메타태그를 미리보기로 표시합니다.

## 점수 산정 기준

| 항목 | 감점 조건 | 최대 감점 |
|------|-----------|-----------|
| Title 길이 | 60자 초과 시 건당 -1점 | 25점 |
| H1 누락 | H1 없는 페이지 건당 -2점 | 40점 |

## 기술 스택

- HTML / Vanilla JS
- [Tailwind CSS](https://tailwindcss.com/) (CDN)
- [SheetJS (xlsx)](https://sheetjs.com/) — 엑셀 파싱
- [Jina AI Reader](https://r.jina.ai/) — URL 메타 크롤링 (CORS 우회)
