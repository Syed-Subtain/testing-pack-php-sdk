# API

```php
$aPIController = $client->getAPIController();
```

## Class Name

`APIController`


# Get Items by Status

Retrieve a list of items based on their status.

```php
function getItemsByStatus(string $status): array
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | [`string(StatusEnum)`](../../doc/models/status-enum.md) | Template, Required | The status of the items to filter by. |

## Response Type

[`ItemsResponse[]`](../../doc/models/items-response.md)

## Example Usage

```php
$status = StatusEnum::PENDING;

$result = $aPIController->getItemsByStatus($status);
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad request, possibly due to an invalid status value. | `ApiException` |
| 404 | No items found for the given status. | `ApiException` |

