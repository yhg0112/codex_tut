# Post Finder

단일 파일 웹앱 **Post Finder**는 JSONPlaceholder 게시글을 검색하고 즐겨찾기를 관리할 수 있는 프로젝트입니다.

## 실행 방법
1. 저장소 루트에서 간단한 정적 서버를 실행합니다.
   ```bash
   python -m http.server 8000
   ```
2. 브라우저에서 [http://localhost:8000/index.html](http://localhost:8000/index.html) 로 접속합니다.

또는 파일 탐색기에서 `index.html`을 더블 클릭하여 바로 열 수 있습니다.

## 주요 기능
- JSONPlaceholder API(`https://jsonplaceholder.typicode.com/posts`)에서 게시글을 불러옵니다.
- 제목과 본문을 대상으로 하는 실시간 검색(디바운스 300ms 적용).
- 스크롤 하단 도달 시 자동으로 추가 게시글을 로드하는 무한 스크롤.
- 즐겨찾기(⭐️) 토글 및 `localStorage`를 통한 상태 저장/복원.
- 다크 모드 토글 및 모드 유지.
- 키보드 탐색과 접근성을 고려한 landmark/aria 속성 제공.
- 게시글 클릭 시 `#/post/:id` 해시 라우팅 기반 상세 화면 전환과 즐겨찾기 토글, 뒤로 가기 시 검색·스크롤 상태 유지.
- 로딩 및 오류 상태 표시와 재시도 기능.
