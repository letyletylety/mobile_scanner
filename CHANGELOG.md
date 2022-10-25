## 3.0.0-beta.1
Breaking changes:
* [Android] SDK updated to SDK 33.

Features:
* [Web] Add binaryData for raw value.
* [iOS] Captures the last scanned barcode with Barcode.image.
* [iOS] Add support for multiple formats on iOS with BarcodeScannerOptions.
* Add displayValue which returns barcode value in a user-friendly format.
* Add autoResume option to MobileScannerController which automatically resumes the camera when the application is resumed

Other changes:
* [Android] Revert camera2 dependency to stable release
* [iOS] Update barcode scanning library to latest version
* Several minor code improvements

## 1.0.0 (2022-10-25)


### Features

* add formats selector ([4b55b0f](https://github.com/letyletylety/mobile_scanner/commit/4b55b0f1de195107d53952640b12074adaa3f8d5))
* add image picker from gallery for android ([e6b37c6](https://github.com/letyletylety/mobile_scanner/commit/e6b37c69b4e1738c7c026cc315a9e8b498d42a68))
* add local image scanner for Android and iOS ([79c1acf](https://github.com/letyletylety/mobile_scanner/commit/79c1acfa528599a418e4e086d9b39ad708e88e13))
* add macos support ([c1abba2](https://github.com/letyletylety/mobile_scanner/commit/c1abba225fadb1f8449ff00cb60dc80dd675874b))
* add web support ([0cd88ec](https://github.com/letyletylety/mobile_scanner/commit/0cd88eca7bb9d7302ba0c26fcc1c50083aba10c5))
* allow duplicates parameter ([d21e15d](https://github.com/letyletylety/mobile_scanner/commit/d21e15d35e162092c1fb4cf15b442a4e4df7462e))
* enable displayValue ([673d335](https://github.com/letyletylety/mobile_scanner/commit/673d33569a540b604f3ff2ffbe6bdf253bac96f4))
* fix android scanner, torch, switch camera and much more ([0442a5f](https://github.com/letyletylety/mobile_scanner/commit/0442a5f75525cc796c9158a2ba96b34cc91164ae))
* update web integration ([80364d0](https://github.com/letyletylety/mobile_scanner/commit/80364d055c544c507ef9e2461850f31bc258b9d4))


### Bug Fixes

* bad state stream has already been listened to ([e5a2e5b](https://github.com/letyletylety/mobile_scanner/commit/e5a2e5b7cff946a31764976ab8fd7f4926254778))
* Handle all cases when a controller should be initialized and disposed ([2872265](https://github.com/letyletylety/mobile_scanner/commit/2872265f237afac12a22927d4d122684e1fe0783))
* should check for the raw bytes instead of string, in case of a malformed utf8 string ([a563906](https://github.com/letyletylety/mobile_scanner/commit/a5639060a387f9bcaa0710b0acd0e4abff36ef97))
* use correct package name in `AndroidManifest.xml` in example ([1e85d8e](https://github.com/letyletylety/mobile_scanner/commit/1e85d8ed20b4e294b4b0fe0513ed4936e79eac3f))

## 2.0.0
Breaking changes:
This version is only compatible with flutter 3.0.0 and later.

## 1.1.2-play-services
This version uses the MLKit play-services model on Android in order to save space.
With the example app, this version reduces the release version from 14.9MB to 7MB.
More information: https://developers.google.com/ml-kit/vision/barcode-scanning/android

## 1.1.2
This version is the last version that will run on Flutter 2.x

Bugfixes:
* Changed onDetect to be mandatory.

## 1.1.1-play-services
This version uses the MLKit play-services model on Android in order to save space.
With the example app, this version reduces the release version from 14.9MB to 7MB.
More information: https://developers.google.com/ml-kit/vision/barcode-scanning/android

## 1.1.1
Bugfixes:
* Add null checks for Android.
* Update camera dependency for Android.
* Fix return type for analyzeImage.
* Add fixes for Flutter 3.

## 1.1.0
Bugfixes:
* Fix for 'stream already listened to' exception.
* Fix building on Android with latest Flutter version.
* Add several WEB improvements.
* Upgraded several dependencies.

## 1.0.0
BREAKING CHANGES:
This version adds a new allowDuplicates option which now defaults to FALSE. this means that it will only call onDetect once after a scan.
If you still want duplicates, you can set allowDuplicates to true.
This also means that you don't have to check for duplicates yourself anymore.

New features:
* We now have web support! Keep in mind that only QR codes are supported right now.

Bugfixes:
* Fixed hot reload not working.
* Fixed Navigator.of(context).pop() not working in the example app due to duplicate MaterialApp declaration.
* Fixed iOS MLKit version not resolving the latest version.
* Updated all dependencies

## 0.2.0
You can provide a path to controller.analyzeImage(path) in order to scan a local photo from the gallery!
Check out the example app to see how you can use the image_picker plugin to retrieve a photo from
the gallery. Please keep in mind that this feature is only supported on Android and iOS.

Another feature that has been added is a format selector!
Just keep in mind that iOS for now only supports 1 selected barcode.

## 0.1.3
* Fixed crash after asking permission. [#29](https://github.com/juliansteenbakker/mobile_scanner/issues/29)
* Upgraded cameraX from 1.1.0-beta01 to 1.1.0-beta02

## 0.1.2
* MobileScannerArguments is now exported. [#7](https://github.com/juliansteenbakker/mobile_scanner/issues/7)

Bugfixes:
* Fixed application crashing when stop() or start() is called multiple times. [#5](https://github.com/juliansteenbakker/mobile_scanner/issues/5)
* Fixes controller not being disposed correctly. [#23](https://github.com/juliansteenbakker/mobile_scanner/issues/23)
* Catch error when no camera is found. [#19](https://github.com/juliansteenbakker/mobile_scanner/issues/19)

## 0.1.1
mobile_scanner is now compatible with sdk >= 2.12 and flutter >= 2.2.0

## 0.1.0
We now have MacOS support using Apple's Vision framework!
Keep in mind that for now, only the raw value of the barcode object is supported.

Bugfixes:
* Fixed a crash when dispose is called in a overridden method. [#5](https://github.com/juliansteenbakker/mobile_scanner/issues/5) 

## 0.0.3
* Added some API docs and README
* Updated the example app

## 0.0.2
Fixed on iOS:
* You can now set the torch
* You can select the camera you want to use

## 0.0.1
Initial release!
Things working on Android:
* Scanning barcodes using the latest version of MLKit and CameraX!
* Switching camera's
* Toggling of the torch (flash)

Things working on iOS:
* Scanning barcodes using the latest version of MLKit and AVFoundation!
