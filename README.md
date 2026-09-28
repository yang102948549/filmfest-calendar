# 영화제 운영 캘린더

3학년 8학급의 영화제 수업 일정(학교 일정 · 교과 수업 · 외부 강사)과 외부강사 차시 진도를 여럿이 함께 관리하는 공유 달력입니다.

- 페이지: `index.html` 한 파일 (GitHub Pages로 배포)
- 데이터: Firebase 프로젝트 `filmfest-calendar-yang`의 Firestore (서울 리전)
  - 컬렉션 `filmfest_events`, `filmfest_progress`, `filmfest_settings`
  - 로그인 없이 읽고 쓰며, 형식 검사는 `firestore.rules`에서 합니다.

## 수정과 배포

- 페이지 수정: `index.html`을 고친 뒤 `main` 브랜치에 푸시하면 GitHub Pages에 반영됩니다.
- 보안 규칙 수정: `npx -y firebase-tools@latest deploy --only firestore:rules`
