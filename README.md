# 고려 역사 인물 탐험

초등학교 5학년의 **고려 시대 역사 인물 카드 만들기** 수업을 위한 정적 웹사이트입니다.

## 포함된 내용

- 왕건, 광종, 서희, 양규, 강감찬, 김윤후의 인물 선택 화면
- 클릭하면 열리는 인물별 상세 화면: 인물 그림, 대표 업적 3가지, 어려운 낱말, 생각해 볼 문제, 한 줄 정리
- 핵심 문장 복사 버튼과 이전/다음 인물 탐색 기능
- 데스크톱, 태블릿, 휴대전화에 대응하는 디자인
- **나눔스퀘어라운드** 웹폰트 (온라인 CDN, 연결되지 않으면 기본 글꼴로 대체)
- 외부 로그인, 데이터베이스, 설치 프로그램 불필요

## 파일 구성

```
index.html             # 웹페이지 전체 코드 (내용·디자인·동작)
images/
  wanggeon.png          # 왕건 (사용자 제공 그림)
  gwangjong.png         # 광종 (사용자 제공 그림)
  seohui.png            # 서희 (사용자 제공 그림)
  yanggyu.svg           # 양규 (기존 학습용 삽화)
  ganggamchan.png       # 강감찬 (사용자 제공 그림)
  kimyunhu.png          # 김윤후 (사용자 제공 그림)
README.md
```

## 미리 보기

`index.html`을 크롬 등의 브라우저에서 열면 됩니다. 인터넷 연결이 없어도 본문 내용과 인물 그림은 보이지만, 나눔스퀘어라운드 웹폰트는 인터넷에 연결되어 있을 때 적용됩니다.

## GitHub Pages로 공개하기

1. GitHub에서 새 **Public** 저장소를 만듭니다. 예: `goryeo-history`.
2. 압축파일을 풀고, **`index.html`과 `images` 폴더**를 저장소 최상위에 올립니다. 웹에서 `Add file → Upload files`를 선택할 수 있습니다. `README.md`도 함께 올려도 됩니다.
3. 저장소의 `Settings → Pages`로 이동합니다.
4. `Build and deployment`에서 `Source`를 **Deploy from a branch**로 설정합니다.
5. `Branch`를 **main**, 폴더를 **/(root)**로 고르고 `Save`를 누릅니다.
6. 배포가 완료되면 `https://깃허브아이디.github.io/goryeo-history/`와 같은 주소로 접속해 수업에 공유할 수 있습니다. 배포에 몇 분 걸릴 수 있습니다.

**중요:** `index.html`은 반드시 저장소의 최상위(`main` 브랜치의 루트)에 두고 `images` 폴더의 이름과 경로를 유지하세요. 본 사이트는 `#/person/wanggeon` 같은 주소로 인물별 화면을 구분하므로 GitHub Pages에서 새로고침해도 정상적으로 열립니다.

## 수정 방법

- 인물 설명, 핵심 업적, 정리 문장: `index.html` 아래쪽의 `const PEOPLE = [...]`를 찾아 수정합니다.
- 인물의 그림: `images/` 아래 PNG 또는 SVG 파일을 바꾸거나, `const PEOPLE`의 `image` 경로를 원하는 그림의 상대 경로로 바꿉니다.
- 페이지의 색과 글씨: `index.html`의 `<style>` 안 `:root` 색상 값을 수정합니다.
- 글꼴: `<head>`에 있는 나눔스퀘어라운드 CDN을 변경할 수 있습니다.

## 자료 출처 및 삽화 안내

인물 설명은 국사편찬위원회 **우리역사넷** 자료를 초등학교 5학년 수준에 맞게 요약·재구성했습니다. 자세한 내용은 인물별 페이지 하단의 **원문에서 더 알아보기**를 통해 확인할 수 있습니다.

**왕건·광종·서희·강감찬·김윤후의 그림은 선생님이 제공한 자료를 사용했습니다. 양규는 기존 학습용 상상화입니다.** 제공된 그림의 제작 시기·출처와 역사적 고증 여부는 별도로 확인해 주세요.

- 왕건: https://contents.history.go.kr/mobile/eh/view.do?code=ganada&levelId=eh_n0220_0010
- 광종: https://contents.history.go.kr/mobile/eh/view.do?levelId=eh_n0230_0010
- 서희: https://contents.history.go.kr/mobile/eh/view.do?code=eh_age_20&levelId=eh_n0250_0010
- 양규: https://contents.history.go.kr/mobile/kc/view.do?levelId=kc_n203010
- 강감찬: https://contents.history.go.kr/mobile/eh/view.do?levelId=eh_n0260_0010
- 김윤후: https://contents.history.go.kr/mobile/eh/view.do?code=ganada&levelId=eh_n0330_0010

글꼴 안내: https://github.com/kingyong9169/NanumSquareRound
