### Version 5.0.0 (13th December 2024)

We're excited to release our major new SDK version (v5). Among many internal improvements, our spoofing protection solution is now included out of the box, reinforcing our commitment to accurate, actionable, and fraud-free data.

To try out SDK v5 in your app, you can follow our new v4 to v5 [migration guide](./MIGRATION.md).

If you are a current Adjust client and have questions about SDK v5, please email [sdk-v5@adjust.com](mailto:sdk-v5@adjust.com).

---

### Version 4.28.0 (2nd April 2021)
#### Changed
- Removed native iOS legacy code.

#### Native SDKs
- [iOS@v4.28.0][ios_sdk_v4.28.0]
- [Android@v4.27.0][android_sdk_v4.27.0]

---

### Version 4.22.1 (5th January 2021)
#### Fixed
- Fixed `AppTrackingTransparency` framework linking issue which caused crashes on pre iOS 14 devices.

#### Native SDKs
- [iOS@v4.24.0][ios_sdk_v4.24.0]
- [Android@v4.25.0][android_sdk_v4.25.0]

---

### Version 4.22.0 (16th December 2020)
#### Added
- Added communication with SKAdNetwork framework by default on iOS 14.
- Added method `deactivateSKAdNetworkHandling` method to `AdjustConfig` to switch off default communication with SKAdNetwork framework in iOS 14.
- Added wrapper method `requestTrackingAuthorizationWithCompletionHandler` to `Adjust` to allow asking for user's consent to be tracked in iOS 14 and immediate propagation of user's choice to backend.
- Added handling of new iAd framework error codes introduced in iOS 14.
- Added sending of value of user's consent to be tracked with each package.
- Added `setUrlStrategy` method to `AdjustConfig` class to allow selection of URL strategy for specific market.
- Added possibility to get cost data information in attribution callback.
- Added `setNeedsCost` method to `AdjustConfig` to indicate if cost data is needed in attribution callback (by default cost data will not be part of attribution callback if not enabled with this setter method).
- Added `setPreinstallTrackingEnabled` method to `AdjustConfig` to allow enabling of preintall tracking (this feature is OFF by default).

**Note**: 4.22.0 ANE is built to support iOS 14 for which you will need **Adobe AIR SDK 33.1.1.300 or higher** and **Xcode 12** to compile your iOS app with.

#### Native SDKs
- [iOS@v4.24.0][ios_sdk_v4.24.0]
- [Android@v4.25.0][android_sdk_v4.25.0]

---

### Version 4.21.1 (4th May 2020)
#### Fixed
- Removed iAd timer from iOS native SDK.

#### Native SDKs
- [iOS@v4.21.3][ios_sdk_v4.21.3]
- [Android@v4.21.1][android_sdk_v4.21.1]

---

### Version 4.21.0 (10th April 2020)
#### Added
- Added support for Huawei App Gallery install referrer.
- Added `disableThirdPartySharing` method to `Adjust` interface to allow disabling of data sharing with third parties outside of Adjust ecosystem.
- Added external device ID support.
- Added support for signature library as a plugin.
- Added more aggressive sending retry logic for install session package.
- Added additional parameters to `ad_revenue` package payload.

#### Changed
- Updated communication flow with `iAd.framework`.

#### Fixed
- Fixed lack of `trackAdRevenue` method definition in iOS extension.

#### Native SDKs
- [iOS@v4.21.1][ios_sdk_v4.21.1]
- [Android@v4.21.1][android_sdk_v4.21.1]

---

### Version 4.18.0 (26th November 2019)
#### Added
- Added 64-bit support to ANE for Android platform.
- Added `trackAdRevenue` method to `Adjust` interface to allow tracking of ad revenue. With this release added support for `MoPub` ad revenue tracking.

#### Native SDKs
- [iOS@v4.18.3][ios_sdk_v4.18.3]
- [Android@v4.18.4][android_sdk_v4.18.4]

---

### Version 4.17.2 (21st February 2019)
#### Changed
- Increased **ios_version_min** to **8.0** from **6.0** (for reference: https://github.com/adjust/adobe_air_sdk/issues/46).

#### Native SDKs
- [iOS@v4.17.1][ios_sdk_v4.17.1]
- [Android@v4.17.0][android_sdk_v4.17.0]

---

### Version 4.17.1 (19th February 2019)
#### Changed
- Using Xcode 10 to build native iOS parts of the ANE.

#### Native SDKs
- [iOS@v4.17.1][ios_sdk_v4.17.1]
- [Android@v4.17.0][android_sdk_v4.17.0]

---

### Version 4.17.0 (14th January 2019)
#### Added
- Added `getSdkVersion()` method to `Adjust` interface to obtain current SDK version string.
- Added `setCallbackId` method on `AdjustEvent` object for users to set custom ID on event object which will later be reported in event success/failure callbacks.
- Added `callbackId` field to event tracking success callback object.
- Added `callbackId` field to event tracking failure callback object.

#### Changed
- Changed usage of `compile` keyword in plugin's `build.gradle` file into `implementation`.
- Updated Android SDK and build tools to `28`.
- Marked `setReadMobileEquipmentIdentity` method of `AdjustConfig` object as deprecated.
- SDK will now fire attribution request each time upon session tracking finished in case it lacks attribution info.

#### Native SDKs
- [iOS@v4.17.1][ios_sdk_v4.17.1]
- [Android@v4.17.0][android_sdk_v4.17.0]

---

### Version 4.14.0 (18th June 2018)
#### Added
- Added deep link caching in case `appWillOpenUrl` method is called natively before SDK is initialised.

#### Changed
- Updated the way how iOS native bridge handles push tokens from Unity interface - they are now being passed directly as strings to native iOS SDK.

#### Native SDKs
- [iOS@v4.14.1][ios_sdk_v4.14.1]
- [Android@v4.14.0][android_sdk_v4.14.0]

---

### Version 4.13.0 (23rd May 2018)
#### Added
- Added `gdprForgetMe` method to `Adjust` interface to enable possibility for user to be forgotten in accordance with GDPR law.

#### Native SDKs
- [iOS@v4.13.0][ios_sdk_v4.13.0]
- [Android@v4.13.0][android_sdk_v4.13.0]

---

### Version 4.12.2 (12th March 2018)
#### Native changes
- Updated iOS SDK to `v4.12.3`.
- Updated Android SDK to `v4.12.4`.

#### Native SDKs
- [iOS@v4.12.3][ios_sdk_v4.12.3]
- [Android@v4.12.4][android_sdk_v4.12.4]

---

### Version 4.12.1 (31st January 2018)
#### Native changes
- https://github.com/adjust/android_sdk/blob/master/CHANGELOG.md#version-4121-31st-january-2018

#### Native SDKs
- [iOS@v4.12.1][ios_sdk_v4.12.1]
- [Android@v4.12.1][android_sdk_v4.12.1]

---

### Version 4.12.0 (31st January 2018)
#### Added
- Added `getAmazonAdId` method to `Adjust` interface.
- Added `setAppSecret` method to `AdjustConfig` interface.
- Added `setReadMobileEquipmentIdentity` method to `AdjustConfig` interface.

#### Native changes
- https://github.com/adjust/ios_sdk/blob/master/CHANGELOG.md#version-4120-13th-december-2017
- https://github.com/adjust/ios_sdk/blob/master/CHANGELOG.md#version-4121-13th-december-2017
- https://github.com/adjust/android_sdk/blob/master/CHANGELOG.md#version-4120-13th-december-2017

#### Native SDKs
- [iOS@v4.12.1][ios_sdk_v4.12.1]
- [Android@v4.12.0][android_sdk_v4.12.0]

---

### Version 4.11.3 (28th September 2017)
#### Added
- **[iOS]** Improved iOS 11 support.

#### Changed
- **[iOS]** Re-added support for Xcode 7 supported iOS SDK versions.
- **[iOS]** Removed iOS connection validity checks.
- **[iOS]** Updated native iOS SDK to version **4.11.5**.

#### Native SDKs
- **[iOS]** [iOS@v4.11.5][ios_sdk_v4.11.5]
- **[AND]** [Android@v4.11.4][android_sdk_v4.11.4]

---

### Version 4.11.2 (10th May 2017)
#### Added
- **[iOS][AND]** Added check if `sdk_click` package response contains attribution information.
- **[iOS][AND]**  Added sending of attributable parameters with every `sdk_click` package.

#### Fixed
- **[iOS]** Fixed suppress log level for iOS platform.

#### Changed
- **[iOS][AND]** Replaced `assert` level logs from SDK with `warn` log level.
- **[AND]** Updated `gradle` version of the `AdjustExtension` project.
- **[iOS]** Updated native iOS SDK to version **4.11.4**.
- **[AND]** Updated native Android SDK to version **4.11.4**.
- **[REPO]** Updated example apps build scripts.

#### Native SDKs
- **[iOS]** [iOS@v4.11.4][ios_sdk_v4.11.4]
- **[AND]** [Android@v4.11.4][android_sdk_v4.11.4]

---

### Version 4.11.1 (27th April 2017)
#### Added
- **[iOS]** Added nullability annotations to public headers for Swift 3.0 compatibility.
- **[iOS]** Added `BITCODE_GENERATION_MODE` to iOS framework for `Carthage` support.
- **[iOS][AND]** Added sending of the app's install time.
- **[iOS][AND]** Added sending of the app's update time.

#### Fixed
- **[iOS]** Fixed not processing of `sdk_info` package type causing logs not to print proper package name once tracked.
- **[AND]** Fixed query string parsing.
- **[AND]** Fixed issue of creating and destroying lots of threads on certain Android API levels (https://github.com/adjust/android_sdk/issues/265).
- **[AND]** Protected `Package Manager` from throwing unexpected exceptions (https://github.com/adjust/android_sdk/issues/266).

#### Changed
- **[AND]** Refactored native networking code.
- **[iOS]** Reverted `AdjustExtension` target to `iOS 6`.
- **[iOS]** Updated native iOS SDK to version **4.11.3**.
- **[AND]** Updated native Android SDK to version **4.11.3**.
- **[REPO]** - Renamed example app folder from `sample` to `example`.
- **[REPO]** Introduced `[iOS]`, `[AND]`, `[WIN]` and `[REPO]` tags to `CHANGELOG` to highlight the platform the change is referring to.

#### Native SDKs
- **[iOS]** [iOS@v4.11.3][ios_sdk_v4.11.3]
- **[AND]** [Android@v4.11.3][android_sdk_v4.11.3]

---

### Version 4.11.0 (19th January 2017)
#### Added
- **[iOS][AND]** Added `adid` property to the attribution callback response.
- **[iOS][AND]** Added `Adjust.getAdid()` method to be able to get adid value at any time after obtaining it, not only when session/event callbacks have been triggered.
- **[iOS][AND]** Added `Adjust.getAttribution()` method to be able to get current attribution value at any time after obtaining it, not only when attribution callback has been triggered.
- **[iOS]** Added method swizzling for iOS platform so that only implemented callbacks in Unity are getting implemented and called in the iOS.
- **[AND]** Added sending of **Amazon Fire Advertising Identifier** for Android platform.
- **[AND]** Added possibility to set default tracker for the app by adding `adjust_config.properties` file to the `assets` folder of your Android app. Mostly meant to be used by the `Adjust Store & Pre-install Tracker Tool` (https://github.com/adjust/android_sdk/blob/master/doc/english/pre_install_tracker_tool.md).

#### Fixed
- **[iOS][AND]** Now reading push token value from activity state file when sending package.
- **[iOS]** Fixed memory leak by closing network session for iOS platform.
- **[iOS]** Fixed `TARGET_OS_TV` pre processor check for iOS platform.

#### Changed
- **[iOS][AND]** Firing attribution request as soon as install has been tracked, regardless of presence of attribution callback implementation in user's app.
- **[iOS]** Saving iAd/AdSearch details to prevent sending duplicated `sdk_click` packages for iOS platform.
- **[AND]** Removed Adobe AIR dependency from native Android submodule to `AndroidExtension` project.
- **[AND]** Changed Maven with Gradle.
- **[iOS]** Updated native iOS SDK to version **4.11.0**.
- **[AND]** Updated native Android SDK to version **4.11.0**.
- **[REPO]** Updated docs.
- **[REPO]** Changed Makefiles with bash scripts.

#### Native SDKs
- **[iOS]** [iOS SDK 4.11.0][ios_sdk_v4.11.0]
- **[AND]** [Android SDK 4.11.0][android_sdk_v4.11.0]

---

### Version 4.10.0 (30th September 2016)
#### Added
- **[iOS]** Added support for iOS 10.
- **[AND]** Added revenue deduplication for Android platform.
- **[iOS][AND]** Added an option for enabling/disabling tracking while app is in background.
- **[iOS][AND]** Added a callback to be triggered if event is successfully tracked.
- **[iOS][AND]** Added a callback callback to be triggered if event tracking failed.
- **[iOS][AND]** Added a callback to be triggered if session is successfully tracked.
- **[iOS][AND]** Added a callback to be triggered if session tracking failed.
- **[iOS][AND]** Added possibility to set session callback and partner parameters with `addSessionCallbackParameter` and `addSessionPartnerParameter` methods.
- **[iOS][AND]** Added possibility to remove session callback and partner parameters by key with `removeSessionCallbackParameter` and `removeSessionPartnerParameter` methods.
- **[iOS][AND]** Added possibility to remove all session callback and partner parameters with `resetSessionCallbackParameters` and `resetSessionPartnerParameters` methods.
- **[iOS][AND]** Added new `Suppress` log level.
- **[iOS][AND]** Added possibility to delay initialisation of the SDK while maybe waiting to obtain some session callback or partner parameters with `delayed start` feature on adjust config instance.
- **[iOS][AND]** Added possibility to set user agent manually on adjust config instance.
- **[iOS][AND]** Added callback method to get deferred deep link content into the app.
- **[iOS][AND]** Added possibility to decide whether the SDK should launch the deferred deep link or not.
- **[iOS][AND]** Added possibility to set user agent manually on adjust config instance.

#### Changed
- **[iOS][AND]** Deferred deep link info will now arrive as part of the attribution response and not as part of the answer to first session.
- **[iOS]** Updated native iOS SDK to version **4.10.1**.
- **[AND]** Updated native Android SDK to version **4.10.2**.
- **[REPO]** Updated docs.

#### Native SDKs
- **[iOS]** [iOS SDK 4.10.1][ios_sdk_v4.10.1]
- **[AND]** [Android SDK 4.10.2][android_sdk_v4.10.2]

---

### Version 4.1.0 (23rd March 2016)
#### Added
- **[iOS]** Added `getIdfa` method for getting `IDFA` on iOS device.
- **[AND]** Added `getGoogleAdId` method for getting `Google Play Services Ad Id` on Android device.
- **[REPO]** Added `CHANGELOG.md`.

#### Changed
- **[iOS]** Renamed `Adjust.framework` to `AdjustSdk.framework`.
- **[iOS]** Removed `MAC MD5` tracking feature for `iOS platform` completely.
- **[iOS]** Updated native iOS SDK to version **4.5.4**.
- **[AND]** Updated native Android SDK to version **4.2.3**.

#### Native SDKs
- **[iOS]** [iOS SDK v4.5.4][ios_sdk_v4.5.4]
- **[AND]** [Android SDK v4.2.3][android_sdk_v4.2.3]

---

### Version 4.0.1 (8th September 2015)
#### Changed
- **[iOS][AND]** Code cleanup.

#### Fixed
- **[iOS][AND]** Removed hard coded environment variable.

#### Native SDKs
- **[iOS]** [iOS SDK v4.2.8][ios_sdk_v4.2.8]
- **[AND]** [Android SDK v4.1.2][android_sdk_v4.1.2]

---

### Version 4.0.0 (2nd September 2015)
#### Added
- **[iOS][AND]** Upgraded Adjust SDK to version `4.0.0`.

#### Changed
- **[iOS]** Updated native iOS SDK to version **4.2.8**.
- **[AND]** Updated native Android SDK to version **4.1.2**.

#### Native SDKs
- **[iOS]** [iOS SDK v4.2.8][ios_sdk_v4.2.8]
- **[AND]** [Android SDK v4.1.2][android_sdk_v4.1.2]

---

### Version 3.4.3 (2nd April 2015)
#### Added
- **[iOS][AND]** Added auxiliary classes to non-native/default target.

#### Native SDKs
- **[iOS]** [iOS SDK v3.4.0][ios_sdk_v3.4.0]
- **[AND]** [Android SDK v3.5.0][android_sdk_v3.5.0]

---

### Version 3.4.2 (10th March 2015)
#### Added
- **[iOS]** Added support for iOS 64 bit.
- **[iOS]** Prefixed names to prevent namespace collisions.

#### Native SDKs
- **[iOS]** [iOS SDK v3.4.0][ios_sdk_v3.4.0]
- **[AND]** [Android SDK v3.5.0][android_sdk_v3.5.0]

---

### Version 3.4.1 (2nd October 2014)
#### Fixed
- **[iOS][AND]** Fixed flash lifecycle events issue.

#### Native SDKs
- **[iOS]** [iOS SDK v3.4.0][ios_sdk_v3.4.0]
- **[AND]** [Android SDK v3.5.0][android_sdk_v3.5.0]

---

### Version 3.4.0 (29th September 2014)
#### Added
- **[iOS][AND]** Added In-App Source Access.
- **[iOS][AND]** Add option to disable and enable the SDK temporarily.

#### Changed
- **[iOS]** Updated native iOS SDK to version **3.4.0**.
- **[AND]** Updated native Android SDK to version **3.5.0**.

#### Native SDKs
- **[iOS]** [iOS SDK v3.4.0][ios_sdk_v3.4.0]
- **[AND]** [Android SDK v3.5.0][android_sdk_v3.5.0]

---

### Version 2.2.2 (24th July 2014)
#### Added
- **[AND]** Added transmission of `Google Ad Identifier` for Android devices.

#### Native SDKs
- **[iOS]** [iOS SDK v2.2.0][ios_sdk_v2.2.0]
- **[AND]** [Android SDK v2.1.6][android_sdk_v2.1.6]

---

### Version 2.2.1 (26th March 2014)
#### Fixed
- **[iOS][AND]** Fixed tracking events and revenue with custom parameters.

#### Native SDKs
- **[iOS]** [iOS SDK v2.2.0][ios_sdk_v2.2.0]
- **[AND]** [Android SDK v2.1.6][android_sdk_v2.1.6]

---

### Version 2.2.0 (5th March 2014)
#### Changed
- **[iOS]** Updated native iOS SDK to version **2.2.0**.

#### Fixed
- **[iOS]** Fixed an issue with calling `trackRevenue` on iOS.

#### Native SDKs
- **[iOS]** [iOS SDK v2.2.0][ios_sdk_v2.2.0]
- **[AND]** [Android SDK v2.1.6][android_sdk_v2.1.6]

---

### Version 2.1.3 (13th January 2014)
#### Changed
- **[iOS]** Updated native iOS SDK to version **2.1.3**.
- **[AND]** Updated native Android SDK to version **2.1.6**.

#### Native SDKs
- **[iOS]** [iOS SDK v2.1.3][ios_sdk_v2.1.3]
- **[AND]** [Android SDK v2.1.6][android_sdk_v2.1.6]

---

### Version 2.1.2 (10th January 2014)
#### Changed
- **[iOS]** Updated native iOS SDK to version **2.1.2**.
- **[AND]** Updated native Android SDK to version **2.1.5**.

#### Native SDKs
- **[iOS]** [iOS SDK v2.1.2][ios_sdk_v2.1.2]
- **[AND]** [Android SDK v2.1.5][android_sdk_v2.1.5]

---

### Version 2.1.1 (26th November 2013)
#### Changed
- **[AND]** Updated native Android SDK to version **2.1.4**.

#### Fixed
- **[AND]** Fixed Android extension build system.

#### Native SDKs
- **[iOS]** [iOS SDK v2.1.1][ios_sdk_v2.1.1]
- **[AND]** [Android SDK v2.1.4][android_sdk_v2.1.4]

---

### Version 2.1.0 (22nd November 2013)
#### Added
- **[iOS][AND]** Initial release of the adjust SDK for Adobe AIR. Supported platforms: `iOS` and `Android`.

#### Native SDKs
- **[iOS]** [iOS SDK v2.1.1][ios_sdk_v2.1.1]
- **[AND]** [Android SDK v2.1.3][android_sdk_v2.1.3]

[ios_sdk_v2.1.1]: https://github.com/adjust/ios_sdk/tree/v2.1.1
[ios_sdk_v2.1.2]: https://github.com/adjust/ios_sdk/tree/v2.1.2
[ios_sdk_v2.1.3]: https://github.com/adjust/ios_sdk/tree/v2.1.3
[ios_sdk_v2.2.0]: https://github.com/adjust/ios_sdk/tree/v2.2.0
[ios_sdk_v3.4.0]: https://github.com/adjust/ios_sdk/tree/v3.4.0
[ios_sdk_v4.2.8]: https://github.com/adjust/ios_sdk/tree/v4.2.8
[ios_sdk_v4.5.4]: https://github.com/adjust/ios_sdk/tree/v4.5.4
[ios_sdk_v4.10.1]: https://github.com/adjust/ios_sdk/tree/v4.10.1
[ios_sdk_v4.10.3]: https://github.com/adjust/ios_sdk/tree/v4.10.3
[ios_sdk_v4.11.0]: https://github.com/adjust/ios_sdk/tree/v4.11.0
[ios_sdk_v4.11.3]: https://github.com/adjust/ios_sdk/tree/v4.11.3
[ios_sdk_v4.11.4]: https://github.com/adjust/ios_sdk/tree/v4.11.4
[ios_sdk_v4.11.5]: https://github.com/adjust/ios_sdk/tree/v4.11.5
[ios_sdk_v4.12.1]: https://github.com/adjust/ios_sdk/tree/v4.12.1
[ios_sdk_v4.12.3]: https://github.com/adjust/ios_sdk/tree/v4.12.3
[ios_sdk_v4.13.0]: https://github.com/adjust/ios_sdk/tree/v4.13.0
[ios_sdk_v4.14.1]: https://github.com/adjust/ios_sdk/tree/v4.14.1
[ios_sdk_v4.17.1]: https://github.com/adjust/ios_sdk/tree/v4.17.1
[ios_sdk_v4.18.3]: https://github.com/adjust/ios_sdk/tree/v4.18.3
[ios_sdk_v4.21.1]: https://github.com/adjust/ios_sdk/tree/v4.21.1
[ios_sdk_v4.21.3]: https://github.com/adjust/ios_sdk/tree/v4.21.3
[ios_sdk_v4.24.0]: https://github.com/adjust/ios_sdk/tree/v4.24.0
[ios_sdk_v4.28.0]: https://github.com/adjust/ios_sdk/tree/v4.28.0

[android_sdk_v2.1.3]: https://github.com/adjust/android_sdk/tree/v2.1.3
[android_sdk_v2.1.4]: https://github.com/adjust/android_sdk/tree/v2.1.4
[android_sdk_v2.1.5]: https://github.com/adjust/android_sdk/tree/v2.1.5
[android_sdk_v2.1.6]: https://github.com/adjust/android_sdk/tree/v2.1.6
[android_sdk_v3.5.0]: https://github.com/adjust/android_sdk/tree/v3.5.0
[android_sdk_v4.1.2]: https://github.com/adjust/android_sdk/tree/v4.1.2
[android_sdk_v4.2.3]: https://github.com/adjust/android_sdk/tree/v4.2.3
[android_sdk_v4.10.2]: https://github.com/adjust/android_sdk/tree/v4.10.2
[android_sdk_v4.11.0]: https://github.com/adjust/android_sdk/tree/v4.11.0
[android_sdk_v4.11.1]: https://github.com/adjust/android_sdk/tree/v4.11.1
[android_sdk_v4.11.3]: https://github.com/adjust/android_sdk/tree/v4.11.3
[android_sdk_v4.11.4]: https://github.com/adjust/android_sdk/tree/v4.11.4
[android_sdk_v4.12.0]: https://github.com/adjust/android_sdk/tree/v4.12.0
[android_sdk_v4.12.1]: https://github.com/adjust/android_sdk/tree/v4.12.1
[android_sdk_v4.12.4]: https://github.com/adjust/android_sdk/tree/v4.12.4
[android_sdk_v4.13.0]: https://github.com/adjust/android_sdk/tree/v4.13.0
[android_sdk_v4.14.0]: https://github.com/adjust/android_sdk/tree/v4.14.0
[android_sdk_v4.17.0]: https://github.com/adjust/android_sdk/tree/v4.17.0
[android_sdk_v4.18.4]: https://github.com/adjust/android_sdk/tree/v4.18.4
[android_sdk_v4.21.1]: https://github.com/adjust/android_sdk/tree/v4.21.1
[android_sdk_v4.25.0]: https://github.com/adjust/android_sdk/tree/v4.25.0
[android_sdk_v4.27.0]: https://github.com/adjust/android_sdk/tree/v4.27.0
