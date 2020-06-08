---
# required metadata
title: List - Alerts API
description: This article describes the list request in Cloud App Security's Alerts API.
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
# List - Alerts API

*Applies to: Microsoft Cloud App Security*

Run the GET or POST request to fetch a list of alerts matching the specified filters.

## HTTP request

```rest
GET /api/v1/alerts/
```

```rest
POST /api/v1/alerts/
```

## Request BODY parameters

| Parameter | Description |
| --- | --- |
| filters | Filter objects with all the search filters for the request, see [alert filters](api-alerts.md#filters) for more details |
| sortDirection | The sorting direction. Possible values are: `asc` and `desc` |
| sortField | Fields used to sort alerts. Possible values are:<br /><br />**date**: The date when then the alert was created<br /><br />**severity**: The severity of the alert |
| skip | Skips the specified number of records |
| limit | Maximum number of records returned by the request |

## Example

### Request

Here is an example of the request.

```rest
curl -XPOST -H "Authorization:<your_token_key>" "https://<tenant_id>.<tenant_region>.contoso.com/api/v1/alerts/" -d '{
  "filters": {
    // some filters
  },
  "skip": 5,
  "limit": 10
  ...
}'
```

### Response

Returns a list of alerts in JSON format.

```json
{
  "total": 5 // total number of records
  "hasNext": true // whether there is more data to show or not.
  "data": [
    // returned records
  ]
}
```

[!INCLUDE [Open support ticket](includes/support.md)]
