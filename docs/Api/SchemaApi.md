# OpenAPI\Client\SchemaApi

All URIs are relative to /api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**modelSchemaGet()**](SchemaApi.md#modelSchemaGet) | **GET** /{model}/schema | Get model schema |


## `modelSchemaGet()`

```php
modelSchemaGet($model): \OpenAPI\Client\Model\ApiModelSchema
```

Get model schema

Returns the schema information for a specific model including fields and relationships

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\SchemaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$model = 'model_example'; // string | Model name

try {
    $result = $apiInstance->modelSchemaGet($model);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SchemaApi->modelSchemaGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **model** | **string**| Model name | |

### Return type

[**\OpenAPI\Client\Model\ApiModelSchema**](../Model/ApiModelSchema.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
