# swipeStory2
Swipe Story (TikTok-style UI Prototype)

TikTok과 유사한 가로(카테고리) + 세로(콘텐츠) 스와이프 인터랙션을 웹 환경에서 구현한 UI 프로토타입입니다.
각 카테고리는 전체 화면을 차지하며, 카테고리 내부에서는 카드 단위로 세로 스크롤이 가능합니다.

📌 주요 특징

가로 스와이프: 카테고리 간 이동 (전체 화면 단위)

세로 스와이프: 카테고리 내 카드(스토리) 탐색

iframe 기반 콘텐츠 로딩: 각 카드별 독립 HTML

카테고리 인디케이터: 현재 위치를 dot UI로 표시

모바일 퍼스트 구조: viewport 기준 반응형 동작

🗂️ 카테고리 구성

현재 총 4개의 카테고리가 구성되어 있습니다.

GHM

Japan Ads

Movies

Books

각 카테고리는 최대 10개의 카드(스토리)를 포함합니다.

📁 디렉토리 구조 예시
/
├─ index.html
├─ main.css
└─ html/
   ├─ GHM/
   │  ├─ 1.html
   │  ├─ 2.html
   │  └─ ...
   ├─ japanAds/
   │  ├─ 1.html
   │  └─ ...
   ├─ movies/
   │  └─ ...
   └─ books/
      └─ ...


index.html : 전체 스와이프 컨테이너 및 네비게이션 로직

main.css : 레이아웃 및 스와이프 UX 스타일

html/*/*.html : 각 카드에 로드되는 개별 콘텐츠

🧠 동작 방식 요약

.horizontal-container

window.innerWidth 기준으로 가로 스크롤

각 섹션은 하나의 카테고리

.vertical-container

세로 스크롤을 통해 카드 탐색

각 카드에는 iframe 삽입

JavaScript

가로 스크롤 위치를 기준으로 현재 카테고리 계산

인디케이터 dot 활성화 상태 업데이트

🚀 실행 방법

별도 빌드 과정 없이 정적 파일로 실행 가능합니다.

# 로컬 서버 예시 (선택)
python -m http.server


브라우저에서 index.html을 직접 열어도 동작합니다.
(iframe 보안 이슈 방지를 위해 로컬 서버 실행 권장)

🎯 활용 목적

TikTok / Reels / Shorts 스타일 UI 프로토타이핑

카드 뉴스, 마이크로 콘텐츠 실험

브랜드 스토리텔링, 광고 크리에이티브 테스트

AI 추천 콘텐츠 UI 실험용 Shell

🔧 향후 확장 아이디어

터치 제스처 감지 (Swipe velocity 기반)

URL hash 기반 딥링크

AI 추천 로직 연동

카드 간 preload / lazy loading

조회수, 체류시간 기반 인터랙션 로그 수집
