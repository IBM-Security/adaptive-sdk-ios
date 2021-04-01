# IBM Security Verify Adaptive SDK for iOS

[![SDK Version](https://img.shields.io/badge/version-1.0.0-lightgray.svg)](https://ibm.biz/ibmsecuritymobileaccesssdk)
![Swift Version](https://img.shields.io/badge/swift-5.1-orange.svg)

This repository contains a sample app to showcase and provide guidance when developing mobile applications with the IBM Security Verify Adaptive SDK. The following steps will help you get started.

[Looking for the Android version?](../android)

<br/>

## Prerequisites

- Download the IBM Security Verify Adaptive SDK for iOS from the [IBM App Exchange](https://exchange.xforce.ibmcloud.com/hub/IdentityandAccess).
<<<<<<< HEAD
- Download and unzip the Trusteer SDK for iOS after [application onboarding](https://docs.verify.ibm.com/verify/docs/on-boarding-a-native-application).
=======
- Download and unzip the Trusteer SDK for iOS after [application onboarding](https://pages.github.ibm.com/ibm-security/iam-docs/adaptive/native-applications/onboarding-a-native-app/onboarding-native-apps-using-adaptive-access).
>>>>>>> master
> NOTE: Confirm with your tenant administrator that Adaptive Access has been enabled for your tenant.
<br/>


## Setup

### Reference the SDK libraries

1\. Clone the sample project in this repository, then launch Xcode by opening the **a2.xcodeproj** file.  Alternatively, launch Xcode and open or create a Swift project.

2\. Open the folder where the SDK's were extracted as part of the prerequisites.
- For the Adaptive SDK, copy the `Frameworks` folder to the folder of your Xcode project.
- For the Trusteer SDK, copy `tazSDK.xcframework` to the `Frameworks` folder of your Xcode project.  

>The `Frameworks` folder should be at the same folder level as the .xcodeproj file.
>

3\. In Xcode, select the top level Project item on the left.  Select the project in the `TARGETS` section.

4\. To reference the frameworks, select the `General` tab along the top of the middle pane.  Scroll down to the section `Frameworks, Libaries, and Embedded Content` and click the **+**.   Click on `Add Other...` and select `Add files...` then navigate to the `Frameworks` folder that was copied to your project. Select the `IBMAdaptiveKit.xcframework`, then click `Open`.

Repeat this step, to add `tazSDK.xcframework` to the project.

### Reference the SDK support files

1\. In your Xcode project, right click a folder and select `Add file to <project>...`

2\. Navigate to the folder where the Trusteer SDK was extracted and select  `default_conf.rpkg`, `manifest.rpkg` and `SDK-S\TrusteerCollectionService.swift`.  Check `Copy items if needed`, then click `Add`.

If you have created a new project, add the following framework references.

```swift
import IBMAdaptiveKit
import tazSDK
```

>You should notice the autocomplete working, the SDK has been imported correctly.
