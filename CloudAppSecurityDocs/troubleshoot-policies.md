---
# required metadata

title: Troubleshooting Cloud App Security policies | Microsoft Docs
description: This article describes the process for troubleshooting policy creation in Cloud App Security.
keywords:
author: rkarlin
ms.author: rkarlin
manager: mbaldwin
ms.date: 12/06/2018
ms.topic: conceptual
ms.prod:
ms.service: cloud-app-security
ms.technology:
ms.assetid: 828cc94a-248b-44f6-a1ba-c28c0a135f8c

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: reutam
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---
# Troubleshooting Microsoft Cloud App Security policies

*Applies to: Microsoft Cloud App Security*

This article describes the process for troubleshooting policy creation in Cloud App Security.

## Troubleshooting
The following chart has the description and resolution for errors you might see for policies.

|Error|Description|Resolution|
|----|----|----|
| **The policy  <*name*> was automatically disabled due to a configuration error**|If you get this error in Microsoft Cloud App Security, it means that you need to fix the configuration of the indicated policy. When you create a Microsoft Cloud App Security policy, you often make use of other objects created within Cloud App Security or the Security and Compliance Center such as IP tags or custom sensitive types. If the IP tag or custom sensitive type you used in the policy is deleted, the policy will automatically be disabled, and you'll receive this error. This message might also indicate a more general configuration error such as a filter that is too complex. |To restore the policy, edit the policy and fix every configuration error mentioned. This error usually means you need to remove any deleted objects from the policy filters and save the policy.|

## Next steps

[Control cloud apps with policies](control-cloud-apps-with-policies.md)

[Premier customers can also choose Cloud App Security directly from the Premier Portal](https://premier.microsoft.com/)

