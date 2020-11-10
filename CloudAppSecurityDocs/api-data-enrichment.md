---
# required metadata
title: Create IP address range - Data Enrichment API
description: This article describes the create IP address range request in Cloud App Security's Data Enrichment API.
keywords:
author: shsagir
ms.author: shsagir
manager: shsagir
ms.date: 03/27/2020
ms.topic: reference
ms.collection: M365-security-compliance
ms.service: cloud-app-security

# optional metadata
ms.suite: ems
---
# Create IP address range - Data Enrichment API

[!INCLUDE [Banner for top of topics](includes/banner.md)]

Run the POST request to add a new IP address range.

## HTTP request

```rest
POST /api/v1/subnet/
```

## Request BODY parameters

| Parameter | Description |
| --- | --- |
| category | The id of the range category |
| subnets | An array of masks as strings (IPv4 / IPv6) |
| organization (Optional) | The registered ISP |
| tags (Optional) | An array of tags (objects with "text" property set with the tag name) - new or existing |

The following categories are currently supported:

| Category | Id |
| --- | -- |
| Corporate | 1 |
| Administrative | 2 |
| Risky | 3 |
| VPN | 4 |
| Cloud provider | 5 |
| Other | 6 |

## Example

### Request

Here is an example of the request.

```rest
curl -XPOST -H "Authorization:Token <your_token_key>" "https://<tenant_id>.<tenant_region>.contoso.com/api/v1/subnet/create_rule/" -d '{
  "name":"range name",
  "category":5,
  "organization":"Microsoft",
  "subnets":[
    "192.168.1.0/24",
    "192.168.2.0/16"
  ],
  "tags":[
    "existing tag"
  ]
}'
```

### Response

Returns the id of the new range as a string.

[!INCLUDE [Open support ticket](includes/support.md)]
