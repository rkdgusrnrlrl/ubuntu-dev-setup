# 우분투 18.04

우분투 18 로 오면서 많은 변화가 있었는데 우선 Xwindow 가 unity 에서 Gnome 으로 바뀌었다. 많은 사람들이 Gnome 을 선호하는데, 이유는 잘 모르지만 Gnome 이 더 낫지 않을까 싶다. 그리고 python 이 드디어 3 이 깔려 있다. 3 또 설치해야 하는 불편함이 줄었다. 그리고 새로운 응용프로그램 방식이 생겼다고 들었는데, 뭐 큰 상관은 없을 것 같다 사실 17에 이미 반영이 됐지만, LTS 가 아니므로 패스

기존에 한글 해결 및 LTS 로 갈아 타기 위해 18 설치를 결정 했다.

USB  부분 에서 막혔는데, `error: zlib decompression failed, data probably corrupt` 가 뜨며 설치가 안됐다. 우분투를 다시 받아보고 USB 를 바꿔보기도 했는데, 격국 USB 를 만들어주는 프로그램  rufus의 버전은 2.17 때로 바꿔 주어 해결 했다. 설치 부터 험난 했다. 기본 언어 설정은 영어로 하고, 키보드를 한글 키보드로 하는 형태로 설치 하였다.

## 크롬

- 역시 처음 설치틑 크롬
- 기본 데스크탑에는 파이어폭스를 쓰지만, 개발시에는 크롬이 더 편한것 같다
- 설치하는 플러그인은 다음과 같다
  - vimium : vim 스타일의 키보드 브라우징
  - diigo : 북마크 수집 서비스 플러그인

## 리눅트 커멘트 유틸

처음에 개발자라면 필수로 설치 하야 할 유틸들이 깔려 있지 않다 그래서 깔아야 하는 데 리스트는 아래와 같다.

- curl : url 테스트 및 파일 다운로드 기능을 겸함
- git : 버전관리 및 Github 사용을 위해서
- vim : 터미널용 에디터는 센스

## 쉘 (zsh)

- 설치 순서는 zsh oh-my-zsh nvm pure 순으로 설치 했음
- zsh 쉘 설치 후 쉘 변경을 잊지 말자
- pure 설치후 `.zshrc` 에 `ZSH_THEME="pure"` 로 변경해 주자

##  한글 설정

- `fcitx` 를 이전에 사용 했는데, 이전에 jetbrain 및 zsh 사용을 못해서 다른 입력기를 썼는다.
- [우분투 18.04 LTS Bionic Beaver를 써보았습니다!](http://hamonikr.org/board_bFBk25/47998) : 18 에서 어떤 입력기를 쓸지는 이글을 참조 했다.
- [가장 스트레스 안받는 우분투 한글입력기, UIM 설치](http://www.kwangsiklee.com/ko/2016/12/%EC%9A%B0%EB%B6%84%ED%88%AC%EC%97%90%EC%84%9C-uim-%ED%95%9C%EA%B8%80%EC%9E%85%EB%A0%A5%EA%B8%B0-%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/) : 설치는 이글을 참조 했다.
- 혹시 몰라 zsh 설치를 먼저 하고 한글 설정 설치를 진행했다.
- 현재 jetbrain IDE, zsh 사용에 문제가 없다.

## NVM

- 이전 설정 참조
- Github 의 레파지토리를 그대로 따라하면 된다.

## JAVA

- 이전 설정 참조

## Gradle

- sdkman 설치
- sdkman 으로 gradle 설치

## Jetbrain Tool box

- 홈페이지
- jetbrain IDE 는 다 이걸로 설치 관리 할 수 있다 
- 이것만 설치 하자

## Typora

- 마크다운 에디터 하나쯤은 써줘야함
- 홈페이지

## D2coding

- [Ubuntu Linux에 코딩용 폰트 설치](http://webnautes.tistory.com/1071) : 폰드 설치 참조
- [naver/d2codingfont](https://github.com/naver/d2codingfont)

## Python3

- 기본!!!
- `venv`로 가상환경 세팅시 `ModuleNotFoundError: No module named 'distutils.core'` 이슈 발생함
  - `sudo apt-get install python3-distutils` 를 쓰면 해결
