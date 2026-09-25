DAY 독립 실행형 PWA 패키지

구성:
- index.html : 앱 본체
- manifest.webmanifest : 독립 실행형 앱 설정
- sw.js : 오프라인 실행용 서비스 워커
- icons/ : 숫자 없는 베이지/세이지 달력 아이콘

설치/배포:
1. 이 폴더의 파일을 GitHub Pages 등 HTTPS 웹 호스팅의 같은 경로에 모두 업로드합니다.
2. 사이트를 한 번 연 뒤 브라우저의 '홈 화면에 추가' 또는 '앱 설치'를 사용합니다.
3. 설치 후에는 manifest의 display=standalone 설정에 따라 주소창 없는 독립 실행형 창으로 열립니다.

주의:
- file:// 로 index.html을 직접 여는 것만으로는 서비스 워커/PWA 설치가 동작하지 않습니다. HTTPS 또는 localhost가 필요합니다.
- 기존 앱 데이터는 브라우저의 IndexedDB에 저장됩니다. 배포 경로(origin)가 바뀌면 기존 데이터와 별개 저장소로 취급될 수 있으므로 JSON 백업/복원을 이용하세요.
