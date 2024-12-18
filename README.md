# Local Background Remover (Android/IOS)

<img src="https://i.ibb.co/xhtjGsD/Luminosity.png"/>

## Overview

The Background Removal Library is a powerful tool designed to seamlessly remove backgrounds from
images in both Android and iOS platforms.This library provides developers with an easy-to-use
interface to integrate background removal functionality into their mobile applications, enhancing
user experience and enabling a wide range of creative possibilities.

## System requirements

- iOS: 15+
- Android: 4.4+ (SDK 19)

## Features

- Offline Support: Remove backgrounds without internet for quick performance offline.
- Object and Person Detection: Easily remove backgrounds from both objects and people.
- Cross-Platform: Delete backgrounds on Android and iOS.

## Getting started

Add the plugin package to the `pubspec.yaml` file in your project:

`If you only require person detection on iOS,consider using version 0.0.8 to reduce your app's size.`

```yaml
dependencies:
  local_rembg: ^1.1.3
```

Install the new dependency:

```sh
flutter pub get
```

Call the `removeBackground` function in your code:

```dart
Future<LocalRembgResultModel> removeBackground() async {
  LocalRembgResultModel localRembgResultModel = await LocalRembg.removeBackground(
     imagePath: // Your Image Path ,
     imageUint8List: // Your image Uint8List ,
     cropTheImage: // Crop the segmented image (Default true) ,
  );
  return localRembgResultModel;
}
```

## Example

Explore our [Example Project](./example) to see how the Local Rembg SDK can be used in a Flutter
application.

## License Terms

This library is provided under the [Apache License](LICENSE).
