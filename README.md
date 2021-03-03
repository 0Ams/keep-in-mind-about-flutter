# keep-in-mind-about-flutter
```
  flutter 사용하며, 남겨두는 공간
```

# flutter 란
Flutter는 Google에서 개발하고 Mobile World Congress 2018에서 최초 베타 릴리스를 발표하면서 새롭게 소개된 크로스 플랫폼 모바일 앱 개발 프레임워크. 
또한 개발자가 iOS와 Android 두 OS에 대해 고품질 기본 인터페이스를 제작하는 데 도움을 주는 크로스 플랫폼 프레임워크이다.

기존 UI를 모두 버리고 자체적으로 UI를 렌더링하기 때문에 iOS에서 material 디자인과 ripple 애니메이션 을 볼 수 있고 Android 에서 cupertino 디자인을 볼 수 있다.
마치 화면 전체를 2D 그래픽 API로 fillRect 하고 drawText drawImage 해서 앱을 만드는 것처럼 Flutter 엔진이 Skia 기반으로 렌더링 해준다.

![image1](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcAL1ve%2Fbtqz8otgZMg%2F4IMrh95SLT0n6IBkEj3FW1%2Fimg.png)
![image2](https://css-tricks.com/wp-content/uploads/2018/08/flutter-03.jpg)
## 장점
* 통합 개발 환경 지원
* 성능 문제 해결
* 머티리얼 디자인과 쿠퍼티노
* Dart를 사용하지만 Native 코드도 사용

## 단점
* Native API를 Dart에서 직접 호출 불가.
* 특별히 심하게 문제가 되진 않지만 외부 플러그인을 써야한다.
* Air BNB Lotti 사용 불가.
* 웨어러블 디바이스앱에 약하다
* C/C++ 라이브러리 호출이 안됨.
* NDK C/C++ 라이브러리 호출이 Dart에서 안됨.
* 외부 플러그인을 써야하고, 원하는 플러그인이 없다면 만들어야 하는데 이는 쉽지 않다
* 지원되는 플러그인이 부족.

## 그래도 쓰는 이유
* 대세가 되어가고 있다. 
* 국내 레퍼런스는 적지만 해외 레퍼런스의 경우 많다.
* 크로스 플랫폼이 다양하지만 그중에서 그래도 잘나가는 녀석중 하나이다. (1위. react-native, 2위 flutter, 3위 swift)
* 내장된 많은 위젯들을 가지고 있어 좋다.

# install flutter

## 기본설치 tools
* xcode
* flutter
* vscode
* android sdk

## 설치하기 
* [참고 자료](https://flutter-ko.dev/docs/get-started/install/macos)
  * flutter 레퍼런스에 자세하게 설명 되어있음.
```bash
git clone -b stable https://github.com/flutter/flutter.git
flutter upgrade
```

## 설정
 * `~.zshrc` 또는 `~.bashrc`에 path추가.
  * 지속적으로 flutter를 사용하기 위한 path 설정

example) 
```bash
export PATH="/usr/local/opt/sqlite/bin:$PATH"
export PATH="$PATH:~/flutter/bin" # flutter를 다운 받아서 압축을 푼곳
```

## 상태 확인
* doctor 명령어를 활용 하여 설치 상태를 확인 할 수 있다.
```bash
flutter (stable|✔): flutter doctor
Doctor summary (to see all details, run flutter doctor -v):
[✓] Flutter (Channel stable, 1.22.6, on Mac OS X 10.15.7 en-KR)
[✗] Android toolchain - develop for Android devices
    ✗ Unable to locate Android SDK.
      Install Android Studio from: https://developer.android.com/studio/index.html
      On first launch it will assist you in installing the Android SDK components.
      (or visit https://flutter.dev/docs/get-started/install/macos#android-setup for detailed instructions).
      If the Android SDK has been installed to a custom location, set ANDROID_SDK_ROOT to that location.
      You may also want to add it to your PATH environment variable.

[!] Xcode - develop for iOS and macOS (Xcode 12.4)
    ✗ Xcode requires additional components to be installed in order to run.
      Launch Xcode and install additional required components when prompted or run:
        sudo xcodebuild -runFirstLaunch
    ✗ CocoaPods not installed.
        CocoaPods is used to retrieve the iOS and macOS platform side's plugin code that responds to your plugin usage
        on the Dart side.
        Without CocoaPods, plugins will not work on iOS or macOS.
        For more info, see https://flutter.dev/platform-plugins
      To install:
        sudo gem install cocoapods
[!] Android Studio (not installed)
[✓] VS Code (version 1.53.2)

[!] Connected device
    ! No devices available

! Doctor found issues in 4 categories.
```
* 문제 있는 요소에 대해 설치 하는 가이드나 문제점 해결을 위해서 찾아 해결을 하면 된다.

## 시뮬레이터설정
appstore 에서 xcode는 별도 설치해준다
```bash
xcode-select --switch /Applications/Xcode.app/Contents/Developer
open -a Simulator
flutter run
```

## IOS 배포
```bash
brew update
brew install --HEAD usbmuxd
brew link usbmuxd
brew install --HEAD libimobiledevice
brew install ideviceinstaller ios-deploy cocoapods
pod setup
```

## Debugging 하기
`launch.json`에 아래와 같이 추가
```bash
{
  "version": "0.0.1",
  "configurations": [
    {
      "name": "Flutter",
      "request": "launch",
      "type": "dart"
    }
  ]
}
```

## sample
많은 예제들을 찾아볼 수 있음.
1. https://github.com/flutter/samples
2. https://github.com/iampawan/FlutterExampleApps
   * 종류별로 기본 템플릿 앱이 많음
   * 공부 하는데도 사용하는데도 좋을듯함
3. https://gallery.flutter.dev/
   * 템플릿 가져다 쓸 수 있는 사이트
4. https://fluttercommunity.slack.com/ssb/redirect
   * flutter slack 채널 이야기 나누거나 피드백 받기 좋음

## Ios 개발 with flutter
[Video Label](https://www.youtube.com/watch?v=3PdUaidHc-E&feature=youtu.be)