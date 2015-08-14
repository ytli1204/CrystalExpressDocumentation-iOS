## Requirements
- CrystalExpress works on iOS 7.0 and above.

## Before SDK integration
- Make sure you have get CrystalExpress.plist from Intowow. It will look like this.
    - If you don't have `Crystal_Id`, please contact Intowow to request one for you app.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
  <key>Crystal_Id</key>
  <string>2a317bd038f742a082ee284b478a8e37</string>
</dict>
</plist>
```

## Installation
### Using Cocoapods
- We strongly recommand you to use Cocoapods to integrate with CrystalExpress.
- Add the following code in Podfile
```
pod "CrystalExpressSDK", '~> 1.3'
```
- `pod update` or `pod install`
- Open workspace that pod generate for you, you're ready to use CrystalExpress
- Here's a [sample project](https://github.com/roylo/CrystalExpressSample)

### Manual integration
1. In project build phases "Link Binary With Libraries", add CrystalExpressSDK-x.x.x.a static library
    - [CrystalExpressSDK-1.3.7](https://s3-ap-northeast-1.amazonaws.com/intowow/ios_manual_sdk/CrystalExpressSDK-1.3.7.zip)
2. Add source files to your project
3. Make sure you have the following frameworks added in Build phases
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
4. Add `-ObjC` in TARGETS -> Build Settings -> Linking -> Other Linker Flags
5. Add the following files to your project
    - CrystalExpress.plist
6. You can now start using CrystalExpress lib.

## Change Crystal id
- After setup SDK, change Crystal_Id in CrystalExpress.plist into your app's crystal_id