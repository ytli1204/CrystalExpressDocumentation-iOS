## Installation
### Using Cocoapods
- We strongly recommand you to use Cocoapods to integrate with
CrystalExpress.
- Add the following code in Podfile
```
pod "CrystalExpressSDK", '~> 1.2'
```
- `pod update` or `pod install`
- Open workspace that pod generate for you, you're ready to use CrystalExpress
- Here's a [sample project](https://github.com/roylo/CrystalExpressSample)

### Manual integration
1. In project build phases "Link Binary With Libraries", add CrystalExpressSDK-x.x.x.a static library
    - [CrystalExpressSDK-1.2.3](http://intowow-demo.oss-cn-beijing.aliyuncs.com/ios_manual_sdk%2FCrystalExpressSDK-CN-1.2.3.zip)
1. Add header file to your project
1. Make sure you have the following frameworks added in Build phases
    - Securty.framework
    - CFNetwork.framework
    - MessageUI.framework
    - MobileCoreServices.framework
    - SystemConfiguration.framework
    - AdSupport.framework
    - libz.dylib
    - libc++.dylib
    - CoreTelephony.framework
    - CoreMedia.framework
    - libsqlite3.dylib
    - AVFoundation.framework
    - libicucore.dylib
1. Add `-ObjC` in TARGETS -> Build Settings -> Linking -> Other Linker Flags
1. Add the following files to your project
    - CrystalExpress.plist
1. You can now start using CrystalExpress lib.

## Test CrystalExpress SDK
- First initalize SDK
```objc
[I2WAPI initWithVerboseLog:YES isTestMode:NO];
```

- Check whether SDK is ready to serve
```objc
BOOL isSDKServing = [I2WAPI isAdServing];
```