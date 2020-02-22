
# 애플리케이션 배포

## iOS 애플리케이션 배포

### 1. 홈브루 설치
* 홈브루: 맥용 패키지 관리자
* [홈브루 사이트](https://brew.sh/)
* 설치 확인: `brew --version`

### 2. 노드 설치
* 홈브루로 설치: `brew install node`
* 설치 확인: `node --version`
* 노드 패키지 매니저 설치 확인: `npm --version`

### 3. 왓치맨 설치
* 홈브루로 설치: `brew install watchman`
* 설치 확인: `watchman -version`

### 4. 리액트 네이티브 CLI 설치
* npm으로 설치: `npm install -g react-native-cli`
* 설치 확인: `react-native --version`

### 5. Xcode 설치
* Xcode: IOS 개발 툴
* [Xcode 다운로드 링크](https://apps.apple.com/us/app/xcode/id497799835?mt=12)

### 6. 코코아포드 설치
* 코코아포드: IOS 개발에 사용되는 의존성 관리자
* 설치:`sudo gem install cocoapods`
* 설치 확인: `pod --version`

### 7. 자바 개발 킷 설치
* 안드로이드 개발하기 위해 자바 필요
* 홈브루로 설치 : `brew tap AdoptOpenJDK/openjdk && brew cask install adoptopenjdk8`
* 설치 확인: `java -version`
* 자바 컴파일러 설치 확인: `javac -version`

### 8. 안드로이드 스튜디오 설치
* 안드로이드 스튜디오: 안드로이드 모발 앱 개발 툴
* [안드로이드 스튜디오 다운로드 사이트](https://developer.android.com/studio/index.html)
* `~/.bash_profile`에 환경 설정
    > `export ANDROID_HOME=안드로이드 SDK 위치/Android/sdk`
    > `export PATH=$PATH:$ANDROID_HOME/emulator`
    > `export PATH=$PATH:$ANDROID_HOME/tools`
    > `export PATH=$PATH:$ANDROID_HOME/tools/bin`
    > `export PATH=$PATH:$ANDROID_HOME/platform-tools`
* 설치 확인: `adb`

---

## Android OS 배포

### 1. 초코렛티 설치
* 초코렛티: 윈도우즈 패키지 매니저
* [초코렛티 다운로드 사이트](https://chocolatey.org/)
* 설치 확인: `choco -version`
  
### 2. 노드 설치
* 초코로 설치: `choco install -y nodejs.install`
* 설치 확인: `node --version`
* 노드 패키지 매니저 설치 확인: `npm --version`

### 3. 파이썬 설치
* 리액트 네이티브 빌드 시스템은 파이썬에 의존 (맥은 기본적으로 설치되어있음)
* 초코로 설치: `choco install -y python2`
* 설치 확인: `python --version`

### 4. 자바 개발 킷 설치
* 안드로이드 개발하기 위해 자바 필요
* 초코로 설치: `choco install -y jdk8`
* 설치 확인: `java -version`
* 자바 컴파일러 설치 확인: `javac -version`

### 5. 리액트 네이티브 CLI 설치
* npm으로 설치: `npm install -g react-native-cli`
* 설치 확인: `react-native --version`

### 6. 안드로이드 스튜디오 설치
* [안드로이드 스튜디오 다운로드 페이지](https://developer.android.com/studio/index.html)
* 환경 변수 설정 필요
* 설치 확인: `adb`

