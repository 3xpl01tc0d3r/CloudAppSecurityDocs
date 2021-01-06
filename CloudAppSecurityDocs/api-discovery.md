---
title: Cloud App Security Cloud Discovery API
description: This article provides information about using the Cloud Discovery API.
ms.date: 03/27/2020
ms.topic: reference
---
# Cloud Discovery API

[!INCLUDE [Banner for top of topics](includes/banner.md)]

Cloud Discovery parses system logs provided by the user to detect new and unknown applications in your cloud environment. Use the Cloud Discovery API to automate the uploading of your company's discovery log files. The file upload process consists of 3 API calls which must be called consecutively.

Additionally, Cloud App Security enables you to block access to unsanctioned apps by using your existing on-premises security appliances. Use the Generate block script call to get a dedicated block script and import it to your appliance.

The following lists the supported requests:

- [Initiate file upload](api-discovery-initiate.md)
- [Perform file upload](api-discovery-perform.md)
- [Finalize file upload](api-discovery-finalize.md)
- [Generate block script](api-discovery-script.md)
- List continuous reports
- List continuous report categories
- List app tags
- Create app tag
- Delete app tag

[!INCLUDE [Open support ticket](includes/support.md)]
