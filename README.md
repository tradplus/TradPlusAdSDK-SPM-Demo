# TradPlusAdSDK-SPM-Demo

TradPlus iOS 广告 SDK 的 **Swift Package Manager** 集成示例工程。

- SPM 集成示例：本仓库（无需 CocoaPods）
- CocoaPods 集成示例：[tradplus-ios-demo](https://github.com/tradplus/tradplus-ios-demo)

命名与官方 SPM 包保持一致（`TradPlusAdSDK-SPM`、`TradPlusAdSDK-SPM-AdMob` 等），SDK 包与 Demo 分离，参考 Google 的 [swift-package-manager-google-mobile-ads](https://github.com/googleads/swift-package-manager-google-mobile-ads) + [googleads-mobile-ios-examples](https://github.com/googleads/googleads-mobile-ios-examples) 模式。

## 要求

- Xcode 15+
- iOS 15.0+
- 直接打开 `TradPlusDemo.xcodeproj`（无需 CocoaPods）

## 已集成的 SPM 包（15.16.0）

| 包 | 说明 |
|---|---|
| [TradPlusAdSDK-SPM](https://github.com/tradplus/TradPlusAdSDK-SPM) | 主 SDK |
| TradPlusAdSDK-SPM-AdMob | AdMob |
| TradPlusAdSDK-SPM-Meta | Meta Audience Network |
| TradPlusAdSDK-SPM-AppLovin | AppLovin MAX |
| TradPlusAdSDK-SPM-Unity | Unity Ads |
| TradPlusAdSDK-SPM-HyBid | Verve / HyBid |
| TradPlusAdSDK-SPM-Mintegral | Mintegral |
| TradPlusAdSDK-SPM-GoogleIMA | Google IMA |
| TradPlusAdSDK-SPM-Pangle | Pangle Global |
| TradPlusAdSDK-SPM-Vungle | Liftoff Monetize (Vungle) |
| TradPlusAdSDK-SPM-Yandex | Yandex |
| TradPlusAdSDK-SPM-TaurusX | TaurusX |
| TradPlusAdSDK-SPM-Moloco | Moloco |
| TradPlusAdSDK-SPM-Chartboost | Chartboost |
| TradPlusAdSDK-SPM-Ogury | Ogury |
| [TPMediationHelper](https://github.com/tradplus/pod_TPMediationHelper_sdk) | 测试与排查工具 `1.4.1` |

> `TPCrossAdapter` 已默认包含在 `TradPlusAdSDK-SPM` 主包中，无需单独添加。

## 快速开始

```bash
cd TradPlusAdSDK-SPM-Demo
open TradPlusDemo.xcodeproj
```

命令行构建：

```bash
xcodebuild -project TradPlusDemo.xcodeproj -scheme TradPlusDemo \
  -destination 'generic/platform=iOS Simulator' \
  -resolvePackageDependencies build
```

## 测试工具

右上角「测试工具」按钮：

```objc
#import <TPMediationHelper/TPMediationHelper.h>
[TPMediationHelper open];
```

## 工程配置

- **Other Linker Flags**: `-ObjC`
- **Deployment Target**: iOS 15.0
- App ID / 广告位 ID 见 `TradPlusDemo/AppDelegate.m`
