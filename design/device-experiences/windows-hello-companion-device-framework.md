---
title: Windows Hello and Companion Device Framework
description: Windows Hello works with CDF
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'

ms.date: 05/02/2017
ms.topic: article


---

# Windows Hello and Companion Device Framework

Windows Hello works with the [Companion Device Framework](https://msdn.microsoft.com/en-us/windows/uwp/security/companion-device-unlock) to enhance the user authentication experience. Using the Windows Hello companion device framework, a companion device can provide a rich experience for Windows Hello even when biometrics are not available (e.g., if the Windows 10 desktop lacks a camera for face authentication or fingerprint reader device, for example).

**Note** Microsoft will be deprecating the Windows Hello companion device framework in the future and will publish the date early to ensure customers have adequate lead time to deploy alternative solutions.

**Note** The Windows Hello companion device framework is a specialized feature not available to all app developers. To use this framework, your app must be specifically provisioned by Microsoft and list the restricted secondaryAuthenticationFactor capability in its manifest. To obtain approval, contact cdfonboard@microsoft.com.
