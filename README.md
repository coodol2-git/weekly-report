# 분석지원팀 주간보고 — GitHub Pages 배포본

v9의 개인별 폴더 저장 방식을 웹에서 사용하는 정적 사이트입니다. 별도 빌드나 npm 설치가 필요 없습니다.

## 포함된 파일

| 파일 | 용도 |
| --- | --- |
| `index.html` | 실제 주간보고 화면 |
| `.nojekyll` | HTML을 그대로 게시하도록 설정 |
| `.gitignore` | CSV·계정·보고서 폴더의 Git 추가 방지 |
| `README.md` | 게시 및 사용 안내 |

압축파일은 반드시 먼저 풀어 주세요. GitHub 저장소 최상위에 `index.html`이 있어야 합니다.

## GitHub 웹 화면에서 게시하기

1. GitHub에 로그인하고 새 저장소를 만듭니다. 이름 예: `weekly-report`.
2. GitHub Free의 Pages는 Public 저장소에서 사용할 수 있습니다. 비공개 저장소의 Pages 지원 여부는 계정 요금제에 따라 다릅니다. 일반 Pages 사이트는 웹에서 공개되므로 직원 이름·업무분장 등 양식에 포함된 내용도 방문자가 볼 수 있습니다.
3. 저장소의 파일 업로드 화면을 엽니다. 기존 저장소는 `Add file → Upload files`, 새 빈 저장소는 `uploading an existing file` 링크를 사용합니다.
4. 압축을 푼 `index.html`, `README.md`, `.nojekyll`, `.gitignore`를 저장소 최상위에 올리고 커밋합니다. 폴더째 올려 `weekly-report/index.html`처럼 한 단계 안쪽에 들어가지 않도록 확인합니다. 숨김 파일이 보이지 않을 때는 우선 `index.html`과 `README.md`만으로도 게시할 수 있습니다.
5. `Settings → Pages`를 엽니다.
6. `Build and deployment → Source`에서 `Deploy from a branch`를 선택합니다.
7. `Branch`는 `main`, 폴더는 `/(root)`로 선택하고 `Save`를 누릅니다. 기본 브랜치가 다르면 실제 파일을 올린 브랜치를 선택합니다.
8. 게시가 완료되면 Pages 설정에 표시되는 HTTPS 주소를 엽니다. 주소 형태는 `https://계정명.github.io/weekly-report/`입니다.
9. 이후 같은 위치의 `index.html`을 수정·커밋하면 사이트가 다시 게시됩니다.

GitHub 파일 화면의 Preview 또는 Raw 주소가 아니라 **Pages 설정의 게시 주소**를 사용합니다.

## 게시 후 관리자 사용

1. PC Chrome 또는 Edge에서 게시된 HTTPS 주소를 직접 엽니다.
2. 사용 모드에서 `관리자 — 상위 폴더`를 선택합니다.
3. `Drive / NAS 폴더 연결`을 누르고 `G:\내 드라이브\분석지원팀 주간보고` 폴더를 선택합니다. 드라이브 문자는 PC마다 다를 수 있습니다.
4. `개인 폴더 준비`로 개인 폴더 6개와 종합보고 폴더를 만듭니다.
5. Google Drive에서 **상위 폴더는 관리자만**, **개인 폴더는 해당 직원과 관리자만** 접근하도록 공유합니다. 실제 공유 권한은 이 화면이 자동으로 변경하지 않습니다.
6. 관리자 화면은 조회·취합용입니다. 입력란이 읽기 전용인 것은 정상입니다.

## 직원 사용

1. PC의 Google Drive 앱에 본인 Google 계정으로 로그인합니다.
2. 공유받은 본인 폴더를 PC에서 사용할 수 있도록 준비합니다.
3. 게시된 HTTPS 주소를 PC Chrome 또는 Edge로 엽니다.
4. `직원 — 본인 폴더`와 본인 이름을 선택합니다.
5. `Drive / NAS 폴더 연결`에서 본인 이름의 폴더를 선택합니다.
6. 작성 후 `저장`을 누릅니다. CSV는 개인 폴더에 저장되고 Drive 앱이 동기화합니다.

웹 게시 후에도 PC Google Drive 앱과 폴더 선택이 필요합니다. 브라우저에서 Google Drive 서버에 직접 로그인하는 서비스가 아닙니다. 모바일이나 폴더 선택 API를 지원하지 않는 브라우저에서는 현재 저장 방식이 작동하지 않을 수 있습니다.

## 저장 위치와 접근 권한

| 데이터 | 위치 |
| --- | --- |
| 사이트 소스 | GitHub 저장소 |
| 개인 보고서 CSV | 개인별 Drive/NAS 폴더 / 연도 / 주차 / 담당자.csv |
| 이전 저장본 | 개인별 Drive/NAS 폴더 / 연도 / 주차 / 이력 |
| 종합보고 CSV | 관리자 상위 폴더 / 종합보고 / 연도 |
| 임시저장본 | 현재 브라우저의 로컬 저장소 |

**실제 CSV, 종합보고, 이전 계정 파일, Drive 폴더 전체를 GitHub에 업로드하지 마세요.** `.gitignore`는 Git 명령의 추가를 막는 설정이며 GitHub 웹 업로드를 자동 차단하지는 않습니다.

관리자 모드는 화면 기능을 구분하며 Google 관리자를 인증하지 않습니다. 직원의 실제 파일 접근은 Google Drive 공유 권한 또는 NAS 폴더 권한으로 제한해야 합니다. v9는 자체 ID/PW·계정 신청·승인 기능을 사용하지 않습니다.

## 기존 데이터 사용

- Drive에 저장한 CSV는 웹 주소에서도 같은 폴더를 연결하면 사용할 수 있습니다.
- 이전 v8 구조는 관리자의 `v8 CSV 가져오기`로 개인별 폴더에 복사할 수 있습니다. 원본은 유지됩니다.
- 파일로 열던 HTML의 임시저장본은 웹 주소의 임시저장본과 자동 공유되지 않습니다. 기존 화면에서 CSV로 저장한 뒤 웹 화면에서 불러오세요.
- 연결한 폴더는 페이지를 새로 열 때 다시 선택합니다.

## 문제가 생길 때

- **404:** `index.html`이 지정한 브랜치의 최상위에 있는지 확인합니다.
- **폴더 선택 불가:** PC Chrome/Edge에서 Pages의 HTTPS 주소를 직접 열어 사용합니다. 다른 페이지 안의 미리보기로 실행하지 않습니다.
- **입력 불가:** 관리자 모드는 읽기 전용입니다. 연결 해제 후 직원 모드와 본인 폴더를 선택합니다.
- **다른 PC에서 저장본이 보이지 않음:** Drive 동기화 완료 여부와 같은 공유 폴더를 연결했는지 확인합니다.

## 공식 안내

- [GitHub Pages 게시 소스 설정](https://docs.github.com/ko/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
- [GitHub Pages 사이트 만들기](https://docs.github.com/ko/pages/getting-started-with-github-pages/creating-a-github-pages-site)
- [Google Drive 폴더 공유](https://support.google.com/drive/answer/7166529?hl=ko)
