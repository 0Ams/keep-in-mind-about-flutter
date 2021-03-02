# keep-in-mind-about-flutter
```
  flutter 사용하며, 남겨두는 공간
```

# install flutter

## 기본설치 tools
* xcode
* flutter
* vscode
* android sdk

## 설치하기 
* [참고 자료](https://flutter-ko.dev/docs/get-started/install/macos)
  * flutter 레퍼런스에 자세하게 설명 되어있음.

## 설정
 * `~.zshrc` 또는 `~.bashrc`에 path추가.
  * 지속적으로 flutter를 사용하기 위한 path 설정

example) 
```
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

## Ios 개발 with flutter
[Video Label](https://www.youtube.com/watch?v=3PdUaidHc-E&feature=youtu.be)