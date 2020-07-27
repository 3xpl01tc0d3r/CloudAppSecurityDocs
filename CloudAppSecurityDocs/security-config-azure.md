---
# required metadata

title: Get security configuration recommendations for Azure
description: This article provides information about how to get security configuration recommendations in Cloud App Security by integrating with Azure Security Center.
keywords:
author: shsagir
ms.author: shsagir
manager: shsagir
ms.date: 06/29/2020
ms.topic: conceptual
ms.collection: M365-security-compliance
ms.prod:
ms.service: cloud-app-security
ms.technology:

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: reutam
ms.suite: ems
#ms.tgt_pltfrm:
ms.custom: seodec18

---
# Security configuration for Azure

*Applies to: Microsoft Cloud App Security*

Microsoft Cloud App Security provides you with a security configuration assessment of your Azure environment. The assessment, powered by Azure Security Center, provides recommendations for missing configuration and security control.

## Enable security configuration recommendations

To use this feature, you need the appropriate permissions in Azure AD and in the Azure portal. By default, the Azure AD Global administrator role doesn't provide you with access to Azure subscriptions. Elevate your permissions to grant access to Azure subscriptions for yourself and other users.

> [!IMPORTANT]
> We recommend that you disable the elevation after you complete the following process.

## How to enable Azure security recommendations

To enable security configuration recommendations in Microsoft Cloud App Security:

1. <a href="https://docs.microsoft.com/azure/security-center/security-center-management-groups" target="_blank">Gain tenant-wide visibility for Azure Security Center</a>. This process includes:

    - Granting yourself and all the other Microsoft Cloud App Security administrators you want to grant access to this page, the role of Reader for all subscriptions.
    - Assigning the role on the root management group in Azure Security Center
    - Elevating your Azure AD Global administrator to grant access to Azure subscriptions.
    - The article describes the process for becoming a Security administrator. For this integration to work, the minimum permissions you need are **Reader**.

1. Make sure to open <a href="https://ms.portal.azure.com/#blade/Microsoft_Azure_Security/SecurityMenuBlade/0" target="_blank">Azure Security Center</a> for the changes to take effect.

## How to view Azure security recommendations

1. In Cloud App Security, browse to **Investigate** > **Security configuration**, and then select the **Azure** tab.

    > [!NOTE]
    > It might take up to 15 minutes before your changes take effect.

    ![security configuration menu](media/security-configuration-menu.png)

1. You can filter the recommendations by type, by resource, and by subscription. Additionally, you can click on the security configuration icon ![ASC icon](media/asc-icon.png) to open the recommendation in Azure Security Center for more information and to deep dive into the recommendation.

For information about how to implement security recommendations, see [Managing security recommendations in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-recommendations).

    > [!NOTE]
    > To make investigation even simpler, you can create custom queries and save them for later use. After you've finished building your query, click the **Save as** button in the top right corner of the filters.

![security configuration](media/security-configuration-azure.png)

## Next steps

> [!div class="nextstepaction"]
> [Control cloud apps with policies](control-cloud-apps-with-policies.md)

[!INCLUDE [Open support ticket](includes/support.md)]
