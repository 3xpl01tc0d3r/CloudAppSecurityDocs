---
# required metadata

title: Import user groups from connected apps | Microsoft Docs
description: This topic provides instructions for importing your user groups into Cloud App Security.
keywords:
author: rkarlin
ms.author: rkarlin
manager: mbaldwin
ms.date: 1/15/2018
ms.topic: get-started-article
ms.prod:
ms.service: cloud-app-security
ms.technology:
ms.assetid: 87b831ef-5977-4df8-bed3-3ee54a8adbb5

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: reutam
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

   
# Import user groups

When you connect apps using API connectors, Cloud App Security enables you to import user groups, for example from Office 365 and Azure Active Directory.
There are two types of user groups: 
- Automatic groups </br>Automatic groups are created by default by Cloud App Security. For example, there is an automatic user group called **External** which combines all users from all apps who are external to your organization and have access to files or were in user activities in your tenant.
 The following automatic groups exist in Cloud App Security:
  - External
  - Dropbox administrator
  - Office 365 administrator
  - G Suite administrator
  - Box administrator
  - All Salesforce standard and custom profiles, for example, Salesforce System Administrator. See the full list [here](https://help.salesforce.com/articleView?id=standard_profiles.htm&language=en&type=0).

- Imported groups</br>You can import any group from your connected apps. For example, you can import user groups from Office 365 (Active Directory) and other connected apps. This enables you to look for threats in your org, not by looking at the whole org or at a specific user, but by looking at a specific group. 

Typical scenarios that leverage imported user groups include: you can investigate which docs the HR people look at, or you can check if there's something unusual happening in the executive group, or if someone from the admin group performed an activity outside the US. 
To import user groups:

1. In the menu bar, click the settings icon ![settings icon](./media/settings-icon.png "settings icon") and select **User groups**.
2. Click **Import user group**.

  ![Import user groups](./media/user-groups-add.png)

3. Select the app from which to import the user group. The list of apps will depend on which App Connectors you deployed.
4. Select the group to import. The list of available groups will be a list of all the existing user groups in the app itself. If you want to add a new group, you have to do it directly in the app itself, and then when it appears here, select it.
4. Depending on the size of the group, import can take up to an hour. You can select the option to be notified by email when the import process is complete.
5. Click **Import**. After you import a group, Cloud App Security automatically syncs the group members, just like Active Directory Connect.
7. After the import is complete, from the **User groups** page you can click on a specific group to view a list of all the members of the group. You can also click on any member of the group to further drill down into the details of a specific account and view which apps they use and a summary of the account including graphs of the user and their activity.

Importing groups enables you to select those groups as filters when investigating in the **Activity log** and when creating policies. 

> [!NOTE]
> Only activities performed after importing a user group will be tagged as having been performed by a member of the user group.

For more information on using the User group filters, see [Activities](activity-filters.md).


    
## See Also  
[Set up Cloud Discovery](set-up-cloud-discovery.md)   

[Premier customers can also choose Cloud App Security directly from the Premier Portal.](https://premier.microsoft.com/)  
  
  