# VidyoConnector-xamarin

## Clone Repository
git clone https://github.com/Vidyo/VidyoConnector-xamarin.git

## Overview
VidyoConnector-xamarin is a Xamarin Forms cross platform application which contains three projects:
1. VidyoConnector         : Portable Class Library (PCL) containing shared code that can be used in Xamarin.iOS and Xamarin.Android (and more).
2. VidyoConnector.iOS     : iOS application which leverages the VidyoConnector PCL in building it's UI.
3. VidyoConnector.Android : Android application which leverages the VidyoConnector PCL in building it's UI.

## Acquire VidyoClient iOS and Android SDKs
1. Download the latest Vidyo.io iOS SDK package: https://static.vidyo.io/latest/package/VidyoClient-iOSSDK.zip
2. Move the unzipped VidyoClient-iOSSDK folder to the VidyoConnector-xamarin directory.
3. Download the latest Vidyo.io Android SDK package: https://static.vidyo.io/latest/package/VidyoClient-AndroidSDK.zip
4. Move the unzipped VidyoClient-AndroidSDK folder to the VidyoConnector-xamarin directory.

> Note: SDK version 4.1.20.3 or later is required

## Importing VidyoClient iOS SDK
To use the VidyoClient SDK in a Xamarin.iOS app, perform the following steps:
1.  In the Solution pad, right-click on the Xamarin.iOS project and select "Add" > "Add Existing Folder".
2.  In the file-selection dialog, browse to project subdirectory "VidyoClient-iOSSDK".
3.  Click "Open" to finish the file selection.
4.  Under "Choose files to include in the project", click the checkbox to the left of "VidyoClient-iOSSDK > include > csharp" and select "OK". 
5.  In the Solution pad, right-click on the Xamarin.iOS project and select "Add" > "Add Native Reference".
6.  In the file-selection dialog, browse to project subdirectory "VidyoClient-iOSSDK/lib/ios".
7.  From that directory, select all 6 static library files "lib*.a" and the framework directory "VPX.framework".
8.  Click "Open" to finish the file selection.
9.  In the Solution pad, expand the new "Native References" folder in the project; right-click "libVidyoClient"; and choose "Properties".
10. In that "Properties" pad, go to the "Frameworks" field.
11. Enter the following list of iOS frameworks from Apple:  AudioToolbox AVFoundation CoreLocation CoreMedia SystemConfiguration UIKit

> Note: the above steps are already performed in the VidyoConnector.iOS project in the VidyoConnector-xamarin solution.

## Importing VidyoClient Android SDK
To use the VidyoClient SDK in a Xamarin.Android app, perform the following steps:
1. In the Solution pad, right-click on the Xamarin.Android project and select "Add" > "Add Existing Folder".
2. In the file-selection dialog, browse to project subdirectory "VidyoClient-AndroidSDK".
3. Click "Open" to finish the file selection.
4. Under "Choose files to include in the project", click the checkbox to the left of "VidyoClient-Android" and select "OK". 
5. In the Solution pad, expand the new "VidyoClient-AndroidSDK/lib/android" folder in the project.
6. Right-click on "vidyoclient.jar" and choose "Properties".
7. In that "Properties" pad, go to the "Build action" field and populate it with "AndroidJavaLibrary".
8. Under each of the 4 architecture folders (arm64-v8a, armeabi-v7a, x86, x86_64), right-click "libVidyoClient.so"; and choose "Properties".
9. In that "Properties" pad, go to the "Build action" field and populate it with "AndroidNativeLibrary".

> Note: the above steps are already performed in the VidyoConnector.Android project in the VidyoConnector-xamarin solution.

## Build and Run Application
1. Open VidyoConnector.sln in either Visual Studio or Xamarin Studio version 6.3 or later.
2. Set either VidyoConnector.iOS or VidyoConnector.Android as the Startup Project, depending on which type of device you want to load the application to.
3. Connect an iOS or Android device to the computer via USB.
4. Select the iOS or Android device as the build target of the application.
5. Build and run the application on the iOS or Android device.

