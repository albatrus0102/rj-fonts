귀여운 글꼴 묶음 (결정 #689·#691) — 앱에 묶지 않고, 고를 때 내려받는 파일들

이 폴더의 내용 그대로가 받는 곳(jsDelivr)에 올라가야 앱이 받을 수 있다.
  받는 주소 형식: https://cdn.jsdelivr.net/gh/<소유자>/<저장소>@<태그>/<파일>
  앱의 주소: app/src/main/assets/index.html 의 FT_BASE (지금 albatrus0102/rj-fonts @1.0) — 저장소를 다르게 만들면 이 한 줄과 FT_REV만 맞춘다.
  jsDelivr는 공개 저장소만 서비스한다(이 앱 저장소는 비공개라 쓸 수 없다) → 공개 저장소 하나에 이 폴더의 파일을 그대로 올리고 태그 1.0을 박는다.
  글꼴을 바꾸면(파일 교체·추가) 새 태그로 올리고 FT_BASE의 태그와 FT_REV를 같이 올린다 — 앱은 기대 크기(FT_FONTS의 바이트)와 다르면 받기를 실패로 다룬다.

파일: <id>-subset.woff2 (KS X 1001 한글 2,350자 + 라틴·문장부호·기호 서브셋, WOFF2) · <id>-OFL.txt (SIL OFL 1.1 전문) · manifest.json (바이트·sha256)
원본: Google Fonts(google/fonts 저장소 ofl/<폴더>) — Gowun Dodum · Jua · Single Day · Gaegu(Regular+Bold) · Hi Melody · Gamja Flower · Cute Font. 전부 예약 글꼴명(RFN) 선언 없음.
만든 법: python3 -I scripts/cute-fonts-subset.py <출력> <원본 폴더>  (원본 TTF는 저장소에 넣지 않는다)
시험: test/cute-fonts.test.mjs 가 이 폴더와 앱의 FT_FONTS(크기·해시·한글 2,350자·OFL 전문)가 어긋나지 않는지 본다.
