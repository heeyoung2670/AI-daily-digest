# AI Daily Digest 지침

- 매일 AI 관련 뉴스를 수집하고 한국어로 요약
- 파일명 형식: digests/YYYY-MM-DD.md
- 중립적이고 사실 중심으로 작성
- 각 뉴스에 출처 URL 반드시 포함
- arXiv 논문은 카테고리 목록(arxiv.org/list/...) 대신 반드시 개별 논문 URL(arxiv.org/abs/XXXX.XXXXX) 사용. 논문 제목으로 검색해서 확보할 것
- **독자 수준**: 대상 독자는 SW 개발자이지만 AI 전공자는 아닌 사람이다. LLM, 멀티모달, 에이전틱, 프론티어 모델 등 AI 핵심 용어는 그대로 사용해도 좋다. 지나치게 학술적인 표현보다는 실용적이고 읽기 편한 문체로 작성한다.

## 생성할 파일

매 실행마다 아래 두 파일을 모두 생성 및 업데이트한다.

### 1. `digests/YYYY-MM-DD.md`
마크다운 형식의 날짜별 아카이브 파일.

### 2. `index.html`
GitHub Pages로 서빙되는 웹 페이지. 저장소 루트의 `index.html`을 매일 덮어쓴다.
기존 `index.html`의 HTML 구조와 CSS는 그대로 유지하고, 아래 영역의 내용만 교체한다.

**교체할 영역:**

`#grid-headline` 내부 — 헤드라인 카드들 (최대 5개):
```html
<div class="card">
  <div class="card-num">01</div>
  <div class="card-title">제목</div>
  <div class="card-body">요약 내용</div>
  <a class="card-link" href="출처URL">원문 보기 →</a>
</div>
```

`#grid-research` 내부 — 연구/논문 카드들:
동일한 card 구조 사용. card-num에는 "Research" 텍스트.

`#grid-company` 내부 — 기업 소식 카드들:
동일한 card 구조 사용. card-num에는 "Company" 텍스트.

`#grid-dev` 내부 — 개발자 소식 카드들:
동일한 card 구조 사용. card-num에는 "Dev" 텍스트.

`#insight-text` 내부 — 오늘의 인사이트 한 문장.

## 커밋 워크플로우

뉴스 수집과 파일 작성은 컨텍스트를 많이 소모하므로, **파일을 모두 작성한 즉시** git 작업을 실행한다. 파일 작성과 git 커밋·푸시를 한 턴 안에 연속으로 완료해야 한다. 나중으로 미루지 말 것.

1. 작업 브랜치에서 `digests/YYYY-MM-DD.md` 작성 → 즉시 `index.html` 작성 → 즉시 커밋
2. 커밋 메시지 형식: `digest: YYYY-MM-DD AI news summary`
3. 커밋 직후 작업 브랜치를 원격에 push
4. 작업 브랜치를 main에 머지 후 push까지 자동 완료 (PR 생성 없이 직접 머지)
