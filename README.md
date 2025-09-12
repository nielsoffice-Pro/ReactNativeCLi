# ReactNative-CLI
Installation and build, Deploy CLI 


Installing ReactNative CLI 

* Create folder anywhere in your PC or Mac 
* Name it as you wish this folder is the mobile app project folder
* Then follow the instruction installation React Native CLI with Github 

> https://github.com/react-native-community/cli?tab=readme-ov-file#documentation


```
// remove recent installation CLI : npm uninstall -g react-native-cli @react-native-community/cli

npx @react-native-community/cli@latest init MobileApp
```

... after a while 

```

✔ Downloading template
✔ Copying template
✔ Processing template
✔ Installing dependencies
✔ Do you want to install CocoaPods now? Needed for running iOS project … yes
✔ Installing Ruby Gems
✔ Installing CocoaPods dependencies  (this may take a few minutes)
✔ Initializing Git repository

  
  Run instructions for Android:
    • Have an Android emulator running (quickest way to get started), or a device connected.
    • cd "/Users/apple/Desktop/rjnative/Mapp" && npx react-native run-android

  // This how to run our mobile apps in emulator ISO, but note configuration environment must be done first : ( https://reactnative.dev/docs/set-up-your-environment )
  Run instructions for iOS:
    • cd "/Users/apple/Desktop/rjnative/Mapp"  
    • npx react-native run-ios

    - or -
    • Open Mapp/ios/Mapp.xcworkspace in Xcode or run "xed -b ios"
    • Hit the Run button
    
  Run instructions for macOS:
    • See https://aka.ms/ReactNativeGuideMacOS for the latest up-to-date instructions.

```

Run instructions for iOS:
 <br> • cd "/Users/apple/Desktop/rjnative/Mapp"
 <br> • npx react-native run-ios
    
In your terminal , please kindly patiently waiting until the ISO build Emulator is ready  [  Building the app.... ] 


In case of Error Port Ready to use : ``` Error: listen EADDRINUSE: address already in use :::8081 ``` 
<br> FIXED STEPS: 

```
lsof -i :8081
```

```
 // Result 
 COMMAND   PID  USER   FD   TYPE  DEVICE SIZE/OFF NODE NAME
 node     12345 user   ...  TCP   *:8081 (LISTEN)
```

```
 // replace 12345 from the result running : lsof -i :8081 
 kill -9 12345
```
