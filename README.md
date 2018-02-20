# 우분투 개발 환경 설정

- [ChangJoo-Park/mac-dev-setup](https://github.com/ChangJoo-Park/mac-dev-setup) 를 보고 보통 우분투를 사용 하는 나의 개발 환경에서 세팅 했던 것 들을 정리 하고 자 한다.
- 해당 내용은 우분투 17 을 기준으로 작성 되었다. 근데 내용으로 봐서 별의미가 없을 수 있다.
- 17 의 특징 이라면 python 3 이 기본으로 설치 되어 있다. 기본으로 그놈을 사용 한다.



### 한글 설정

- 개발이고 뭐고 기본은 한/영 전환의 여부이다
- fcitx 를 주로 사용 한다
- 다른 것들은 jetbrain 계열에서 문제가 있거나 chromium 에서 문제 가 있었다.
- fctix 를 적용에 성공 했으나 어느 순간 jetbrains 계열에서 적용이 안되는 이슈를 겪고 있다
  - 덕문에 커밋 메세지를 영어로...

### 개발자 폰트

- 네이년이 하는 것 중에 좋은 것이 개발자 폰트를 만들어 주는 것이다.
- 안쓴다고 크게 불편한 것은 아니지만 개발자로서 상징성 있는 작업이라 꼭 한다.
- 네이년 에서 두가지 개발 폰트를 내 놓았는데, 하나는 나눔고딕코딩 이고 D2coding 이다.
- 나는 이중에 D2coding 을 쓴다.
- 두가지 이유가 있는데 나눔고딕코딩을 줄 간견이 너무 좁다. 그리고 D2coding 이 나눔바른고딕체 여서 한글이 반듯반듯 하다.



## 개발 툴

### Git

- 깃헙을 하기 위해 설치 한다.
- 당신이 생각하고 있는 그방법으로 설치하면 된다.

### Zsh 그리고 oh my zsh

- 우선 fctix 쪽에 이슈가 있어 쓰지 못하고 있다.
- zsh 을 쓰면 한영 전환이 안되는 상황이 발생해 보류 하고 있다.
- 테마는 pure 테마를 선호한다.

### Jetbrains

- 나는 jetbrains 계열 IDE 를 사용 한다.
- 그러므로 [Toolbox App](https://www.jetbrains.com/toolbox/app/?fromMenu) 을 먼저 설치 
  - 위의 앱을 통해 jetbrains  IDE 를 설치 및 버전 관리 프로젝트 관리가 가능하다
  - 그렇다고 많은 기능이 있는 건 아님

### Docker

- 개발환경 구축을 필수 프로그램 이다.

- [Get Docker CE for Ubuntu](https://docs.docker.com/install/linux/docker-ce/ubuntu/) 를 보고 따라 하면 된다.

  - 에러 날 일이 없다....라고 믿고 작업 하자...우선 설치시 에러를 격은 적은 없다.

- 기본적으로 `sudo docker` 와 같이 앞에 `sudo` 를 써줘야 한다.

- 하지만 불편하다 아래의 방법으로 해결 할 수 있다.

  - **sudo 없이 사용하기 **

  ```bash
  $ sudo usermod -aG docker $USER
  $ sudo usermod -aG docker ${사용자명}
  ```

- docker-compose 를 설치하면 여러 컨테이너를 동시에 띄울 수 있다....하지만 `docker stack` 똑같은 기능을 한다 고로 docker-compose 설치 하지 않는 걸 추천 한다. 나는 몰라서 깔았다 

### 알흠다운 텍스트 에디터 vim

- 간혹 순수한 vi 가 깔려 있는 경우가 있다. 냉큼 vim 으로 설치 해주자
- 그렇다 당신이 알고 있는 그 명령어를 써주면 된다. 에이피티겟 인스톨 빔 당연이 수도는 필수
- `vimrc` 와 budle 을 설처하면 텍스트 에디터로 위엄을 갖추게 되지만 해야 할 작업에 비해 수고스러움이 크다.
- 차라리 좋은 텍스트 에디터를 쓰자 VS code 같은...



## 언어

### JAVA

- 그렇다 나는 자바 개발자 였다....하지만 javascript 를 쓰다보니 java 가 그립다 그래서 java를 설치한다.
- 위의 예제는 oracle java8 을 설치 하는 방법이다.

```
$ sudo add-apt-repository ppa:webupd8team/java
$ sudo apt-get update
$ sudo apt-get install oracle-java8-installer
```

- 위의 예제 대로 하면 나중에 버전을 변경할 때 좋다.

### Node.js

- 그렇다 나는 Node.js 개발자다...뭔가 말이 이상하지만, 간단히 무언가 만들기에 좋은 언어이고, 현재 메인 언어다.
- node 를 설치하지 않고 nvm 을 설치 한다.
- [nvm install-script](https://github.com/creationix/nvm#install-script) 를 참고 해서 진행하면 된다 코드만 보면 된다
  - 기본적으로 소스 받아 설치하고 `.bashrc`  같은데에 등록 해주면 된다.
  - 이로서 Node.js 버전 별로 설치를 쉽게 할수 있고 버전을 쉽게 변경 할 수 있다.

### Python

- 그렇다 나는 python 개발자가 아니다.....그래도 잘 쓰고 싶은 언어이다
- 우분투에 기본적으로 python 이 깔려 있다. 17 때 부터는 python 3.6 이 깔려 있다.
- 하지만 실행은 `python3` 라는 슬픈 사실이....
- 17 이전 버전은 python 2 가 깔려 있을 것이다. python3 를 깔아 두는 것을 추천한다.
- 아직 python 을 버전 관리 할 정도로 많이 쓰지 않아 버전 관리 툴을 쓰지 않는다.

