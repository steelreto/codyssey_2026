# 노코드 자동화 과제 — 제출물 구성 및 진행 현황

## 제출물 구성

```
submission/
├── 프로젝트1_비교분석보고서.md      ← Make · n8n 구현 완료 (본문 작성 완료)
├── 프로젝트2_설계및구현문서.md      ← 설계 · 구현 완료 (본문 작성 완료)
└── screenshots/                     ← 캡처 삽입 필요
    ├── project1_make/
    ├── project1_n8n/
    └── project2/
```

## 진행 현황

### ✅ 완료
- [x] 프로젝트 1 — Make 구현 + 분기별 검증 (Tally 폼 → Webhook → Router → Notion/Discord)
- [x] 프로젝트 1 — n8n 구현 + 분기별 검증 (Webhook → IF → Notion/Discord, curl 검증)
- [x] 프로젝트 2 — Make 구현 + 분기별 검증 (Schedule → 환율 API → Notion → 필터 → Discord)
- [x] 프로젝트 1 보고서 본문 작성 완료 (Make·n8n 전체, 비교 5항목, 종합 의견)
- [x] 프로젝트 2 문서 본문 작성 완료

### 🔲 남은 작업 (제출 전)
1. **캡처 삽입** — 두 문서의 📷 표시 위치에 실제 스크린샷 삽입 (아래 캡처 목록 참고)
2. **마스킹 확인** — 아래 체크리스트대로
3. **Discord 웹훅 재발급** — 구현 중 URL이 노출된 이력이 있어 무효화 처리
4. (선택) Markdown → PDF 변환

## 캡처 목록

### 프로젝트 1 — Make (project1_make/)
- [ ] 전체 시나리오 캔버스 (필터 라벨 "3점 이하/4점 이상" 보이게)
- [ ] Router 필터 2개 설정 (Numeric 연산자)
- [ ] Notion 모듈 필드 매핑
- [ ] Tally Integrations — 웹훅 연결
- [ ] 불만족/만족 케이스 실행 (History)
- [ ] Notion DB 기록, Discord 알림

### 프로젝트 1 — n8n (project1_n8n/)
- [ ] n8n 에디터 초기 화면
- [ ] Notion 신규 연결 생성 화면 (토큰 마스킹)
- [ ] 전체 워크플로우 캔버스 (Webhook→IF→두 분기)
- [ ] IF 노드 조건 설정
- [ ] Notion 노드 필드 매핑 (expression 미리보기)
- [ ] IF 실행 결과, Notion DB(Make/n8n 공존), Discord [n8n] 알림

### 프로젝트 2 — Make (project2/)
- [ ] 전체 캔버스 (Schedule→HTTP→Notion→필터→HTTP)
- [ ] HTTP 모듈 (Frankfurter URL)
- [ ] Notion 매핑 / 필터 설정 (≥1430)
- [ ] 초과 케이스(HTTP 실행됨) / 미초과 케이스(⊘0)
- [ ] Discord 알림, Notion 기록, 스케줄 6시간 + 토글 ON

## 민감정보 마스킹 체크리스트 (제출 전 필수)
- [ ] Make 웹훅 URL (hook.us2.make.com/...)
- [ ] Discord 웹훅 URL (discord.com/api/webhooks/...) — 재발급으로 무효화 포함
- [ ] Notion API 시크릿 (n8n용, ntn_...)
- [ ] Notion Data Source ID 일부
- [ ] 계정 이메일 일부 가림
