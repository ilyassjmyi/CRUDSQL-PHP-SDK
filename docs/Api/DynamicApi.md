# OpenAPI\Client\DynamicApi

All URIs are relative to /api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**modelFilterPost()**](DynamicApi.md#modelFilterPost) | **POST** /{model}/filter | Filter entities |
| [**modelGet()**](DynamicApi.md#modelGet) | **GET** /{model} | List and filter entities |
| [**modelIdDelete()**](DynamicApi.md#modelIdDelete) | **DELETE** /{model}/{id} | Delete an entity |
| [**modelIdGet()**](DynamicApi.md#modelIdGet) | **GET** /{model}/{id} | Get an entity by ID |
| [**modelIdPut()**](DynamicApi.md#modelIdPut) | **PUT** /{model}/{id} | Update an entity |
| [**modelPost()**](DynamicApi.md#modelPost) | **POST** /{model} | Create a new entity |


## `modelFilterPost()`

```php
modelFilterPost($model, $filter, $page, $page_size, $sort): \OpenAPI\Client\Model\QueryFilterResponse
```

Filter entities

Filter entities using complex conditions including field expressions, logical operations, and relationship filtering

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DynamicApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$model = 'model_example'; // string | Model name
$filter = new \OpenAPI\Client\Model\QueryQueryFilter(); // \OpenAPI\Client\Model\QueryQueryFilter | Filter conditions
$page = 1; // int | Page number
$page_size = 10; // int | Items per page
$sort = 'sort_example'; // string | Sort field and direction (e.g., name:asc,age:desc)

try {
    $result = $apiInstance->modelFilterPost($model, $filter, $page, $page_size, $sort);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DynamicApi->modelFilterPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **model** | **string**| Model name | |
| **filter** | [**\OpenAPI\Client\Model\QueryQueryFilter**](../Model/QueryQueryFilter.md)| Filter conditions | |
| **page** | **int**| Page number | [optional] [default to 1] |
| **page_size** | **int**| Items per page | [optional] [default to 10] |
| **sort** | **string**| Sort field and direction (e.g., name:asc,age:desc) | [optional] |

### Return type

[**\OpenAPI\Client\Model\QueryFilterResponse**](../Model/QueryFilterResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `modelGet()`

```php
modelGet($model, $page, $page_size, $sort): \OpenAPI\Client\Model\QueryFilterResponse
```

List and filter entities

Get a list of entities. Use query parameters for simple filtering or POST to /filter for complex conditions

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DynamicApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$model = 'model_example'; // string | Model Name
$page = 56; // int | Page number
$page_size = 56; // int | Items per page
$sort = 'sort_example'; // string | Sort field and direction (e.g., name:asc)

try {
    $result = $apiInstance->modelGet($model, $page, $page_size, $sort);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DynamicApi->modelGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **model** | **string**| Model Name | |
| **page** | **int**| Page number | [optional] |
| **page_size** | **int**| Items per page | [optional] |
| **sort** | **string**| Sort field and direction (e.g., name:asc) | [optional] |

### Return type

[**\OpenAPI\Client\Model\QueryFilterResponse**](../Model/QueryFilterResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `modelIdDelete()`

```php
modelIdDelete($model, $id): \OpenAPI\Client\Model\ApiErrorResponse
```

Delete an entity

Delete an entity by its ID

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DynamicApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$model = 'model_example'; // string | Model Name
$id = 'id_example'; // string | Entity ID

try {
    $result = $apiInstance->modelIdDelete($model, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DynamicApi->modelIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **model** | **string**| Model Name | |
| **id** | **string**| Entity ID | |

### Return type

[**\OpenAPI\Client\Model\ApiErrorResponse**](../Model/ApiErrorResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `modelIdGet()`

```php
modelIdGet($model, $id): \OpenAPI\Client\Model\QueryFilterResponse
```

Get an entity by ID

Retrieve a single entity by its ID

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DynamicApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$model = 'model_example'; // string | Model Name
$id = 'id_example'; // string | Entity ID

try {
    $result = $apiInstance->modelIdGet($model, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DynamicApi->modelIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **model** | **string**| Model Name | |
| **id** | **string**| Entity ID | |

### Return type

[**\OpenAPI\Client\Model\QueryFilterResponse**](../Model/QueryFilterResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `modelIdPut()`

```php
modelIdPut($model, $id, $entity): \OpenAPI\Client\Model\QueryFilterResponse
```

Update an entity

Update an existing entity by its ID

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DynamicApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$model = 'model_example'; // string | Model Name
$id = 'id_example'; // string | Entity ID
$entity = new \OpenAPI\Client\Model\QueryEntityWithRelations(); // \OpenAPI\Client\Model\QueryEntityWithRelations | Entity Data

try {
    $result = $apiInstance->modelIdPut($model, $id, $entity);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DynamicApi->modelIdPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **model** | **string**| Model Name | |
| **id** | **string**| Entity ID | |
| **entity** | [**\OpenAPI\Client\Model\QueryEntityWithRelations**](../Model/QueryEntityWithRelations.md)| Entity Data | |

### Return type

[**\OpenAPI\Client\Model\QueryFilterResponse**](../Model/QueryFilterResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `modelPost()`

```php
modelPost($model, $entity): \OpenAPI\Client\Model\QueryFilterResponse
```

Create a new entity

Create a new entity of the specified model type

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DynamicApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$model = 'model_example'; // string | Model Name
$entity = new \OpenAPI\Client\Model\QueryEntityWithRelations(); // \OpenAPI\Client\Model\QueryEntityWithRelations | Entity Data

try {
    $result = $apiInstance->modelPost($model, $entity);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DynamicApi->modelPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **model** | **string**| Model Name | |
| **entity** | [**\OpenAPI\Client\Model\QueryEntityWithRelations**](../Model/QueryEntityWithRelations.md)| Entity Data | |

### Return type

[**\OpenAPI\Client\Model\QueryFilterResponse**](../Model/QueryFilterResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
