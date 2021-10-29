---
title: "Get started with visibility and insights"
f1.keywords:
- NOCSH
ms.author: v-tophillips
author: v-tophillips
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: m365-security-compliance
ms.localizationpriority: high
search.appverid: 
- MOE150
- MET150
description: "Get started with visibility and insights."
---

# Get started with visibility and insights

>*[Microsoft 365 licensing guidance for security & compliance](https://aka.ms/ComplianceSD).*

The first place to get started is the app governance dashboard at [https://aka.ms/appgovernance](https://aka.ms/appgovernance). Note that your sign-in account must have one of [these app governance administrator roles](app-governance-get-started.md#administrator-roles) to view any app governance data.

:::image type="content" source="media\app-governance\mapg-cc-overview.png" alt-text="The app governance overview page in Microsoft 365 Defender." lightbox="media\app-governance\mapg-cc-overview.png":::

You can also access the app governance dashboard from **Office 365 > Microsoft 365 Defender > App governance > Overview page**.

## What’s available on the dashboard

The dashboard contains a summary of the components of the Microsoft 365 app ecosystem in the tenant:

- **Tenant summary**: The count of key app and alert categories.
- **Top alerts**: The 10 most recent active alerts in the tenant
- **Data and resources access**: Mouse over each month column in the graph to see the corresponding value.
  - **Data access over the last four months**: Tracks total data accessed by all apps in the tenant through Graph API over the last four calendar months. Currently only includes Mail and File upload/download usage.
  - **Top resources data access over the last four months**: Data usage over the last four calendar months, broken down by resource type. Currently only includes Mail and File upload/download usage
- **Improve your app protection and governance**: Recommended actions such as creating an app usage or permissions policy.
- **Top apps by categories**: The top apps sorted by these categories:
  
  - **All categories**: Sorts across all available categories.
  - **High privilege**: High privilege is an internally determined category based on platform machine learning and signals.
  - **Overprivileged**: When app governance receives telemetry that indicates that a permission granted to an application has not been used in the last 90 days, that application is overprivileged. App governance must be operating for at least 90 days to determine if any app is overprivileged.  
  - **Unverified**: Applications that have not received [publisher certification](/azure/active-directory/develop/publisher-verification-overview) are considered unverified.
  - **App only**: [Application permissions](/azure/active-directory/develop/v2-permissions-and-consent#permission-types) are used by apps that can run without a signed-in user present. Apps with permissions to access data across the tenant are potentially a higher risk.
  - **New apps**: New Microsoft 365 apps that have been registered in the last seven days.  

## View app insights

One of the primary value points for app governance is the ability to quickly view app alerts and insights. To view insights for your apps:

1. On your app governance portal page, select **Apps**.
1. Use the **Categories** drop down list to select from the following options:
    - All apps
    - High privilege
    - Overprivileged
    - Unverified Publisher
    - App only
    - New apps
1. Select the name of an app to view details. Selecting an app name opens a detail pane on the right as show in the following graphic.

:::image type="content" source="media/app-governance/app-governance-app-insight.png" alt-text="Image showing the details pane for a selected app." lightbox="media/app-governance/app-governance-app-insight.png":::

> [!NOTE]
> The apps listed will depend on the apps present in your tenant.

Saving the query lets you save the defined list of filters in the current view. This could save time when selecting a subset of data in the future.

The details pane also lets you view the usage of the app over the past 30 days, the users who have consented to the app, and the permissions assigned to the app. An administrator could review the activity and permissions of an app that is generating alerts and make a decision to disable the app using the **Disable App** button in the Details pane.

## Next step

[Get detailed insights on a specific app](app-governance-visibility-insights-view-apps.md).
