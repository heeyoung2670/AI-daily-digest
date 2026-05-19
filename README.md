# 🤖 AI Daily Digest

> Claude Code Routines로 구동되는 AI 뉴스 자동 수집 및 요약 시스템

🌐 **[https://heeyoung2670.github.io/AI-daily-digest](https://heeyoung2670.github.io/AI-daily-digest)**

매일 오전 9시, Claude가 자동으로 AI 관련 최신 뉴스를 수집하고 한국어로 요약하여 이 저장소에 커밋합니다.

---

## 📁 구조

```
ai-daily-digest/
├── digests/
│   ├── 2025-05-18.md
│   ├── 2025-05-19.md
│   └── ...
├── CLAUDE.md
├── index.html
└── README.md
```

## 📰 다이제스트 형식

매일 생성되는 요약은 다음 카테고리로 구성됩니다:

| 섹션 | 내용 |
|------|------|
| 🔥 헤드라인 | 오늘의 주요 AI 뉴스 TOP 5 |
| 🧪 연구 동향 | 논문, 연구소 발표 |
| 🏢 기업 소식 | OpenAI, Google, Anthropic, Meta 등 |
| 🛠️ 개발자 소식 | 오픈소스, 새 도구, 프레임워크 릴리즈 |
| 💡 오늘의 인사이트 | 핵심 트렌드 한줄 요약 |

## ⚙️ 작동 방식

이 저장소는 **Claude Code Routines**를 통해 자동으로 업데이트됩니다.

1. 매일 오전 9시(KST), Claude Code Routine이 트리거됨
2. Claude가 웹에서 최신 AI 뉴스를 수집
3. 한국어로 요약 및 분류
4. `digests/YYYY-MM-DD.md` 및 `index.html` 생성 후 커밋

## 🗂️ 지난 다이제스트 보기

[digests/](./digests/) 폴더에서 날짜별로 확인할 수 있습니다.

---

*Powered by [Claude Code Routines](https://code.claude.com/docs/ko/routines)*
