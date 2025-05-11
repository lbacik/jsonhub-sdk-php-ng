# OpenAPI\Client\EntityApi

All URIs are relative to http://localhost:8000, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiEntitiesGetCollection()**](EntityApi.md#apiEntitiesGetCollection) | **GET** /api/entities | Retrieves the collection of entity resources. |
| [**apiEntitiesIdDelete()**](EntityApi.md#apiEntitiesIdDelete) | **DELETE** /api/entities/{id} | Removes the entity resource. |
| [**apiEntitiesIdGet()**](EntityApi.md#apiEntitiesIdGet) | **GET** /api/entities/{id} | Retrieves a entity resource. |
| [**apiEntitiesIdPatch()**](EntityApi.md#apiEntitiesIdPatch) | **PATCH** /api/entities/{id} | Updates the entity resource. |
| [**apiEntitiesPost()**](EntityApi.md#apiEntitiesPost) | **POST** /api/entities | Creates a entity resource. |


## `apiEntitiesGetCollection()`

```php
apiEntitiesGetCollection($qid, $private, $is_owned_by_me, $page, $limit, $properties, $definition, $parent): \OpenAPI\Client\Model\ApiEntitiesGetCollection200Response
```

Retrieves the collection of entity resources.

Retrieves the collection of entity resources.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: access_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\EntityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$qid = 'qid_example'; // string | Filter by slug/id (partial match)
$private = True; // bool | Show only private entities (owned by the current user)
$is_owned_by_me = True; // bool | Show only entities owned by the current user
$page = 1; // int | The collection page number
$limit = 10; // int | The number of items per page
$properties = array('properties_example'); // string[] | Allows you to reduce the response to contain only the properties you need. If your desired property is nested, you can address it using nested arrays. Example: properties[]={propertyName}&properties[]={anotherPropertyName}&properties[{nestedPropertyParent}][]={nestedProperty}
$definition = 'definition_example'; // string | Filter by definition (uuid)
$parent = 'parent_example'; // string | Filter by parent (uuid)

try {
    $result = $apiInstance->apiEntitiesGetCollection($qid, $private, $is_owned_by_me, $page, $limit, $properties, $definition, $parent);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EntityApi->apiEntitiesGetCollection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **qid** | **string**| Filter by slug/id (partial match) | [optional] |
| **private** | **bool**| Show only private entities (owned by the current user) | [optional] |
| **is_owned_by_me** | **bool**| Show only entities owned by the current user | [optional] |
| **page** | **int**| The collection page number | [optional] [default to 1] |
| **limit** | **int**| The number of items per page | [optional] [default to 10] |
| **properties** | [**string[]**](../Model/string.md)| Allows you to reduce the response to contain only the properties you need. If your desired property is nested, you can address it using nested arrays. Example: properties[]&#x3D;{propertyName}&amp;properties[]&#x3D;{anotherPropertyName}&amp;properties[{nestedPropertyParent}][]&#x3D;{nestedProperty} | [optional] |
| **definition** | **string**| Filter by definition (uuid) | [optional] |
| **parent** | **string**| Filter by parent (uuid) | [optional] |

### Return type

[**\OpenAPI\Client\Model\ApiEntitiesGetCollection200Response**](../Model/ApiEntitiesGetCollection200Response.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/ld+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiEntitiesIdDelete()`

```php
apiEntitiesIdDelete($id)
```

Removes the entity resource.

Removes the entity resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: access_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\EntityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | entity identifier

try {
    $apiInstance->apiEntitiesIdDelete($id);
} catch (Exception $e) {
    echo 'Exception when calling EntityApi->apiEntitiesIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| entity identifier | |

### Return type

void (empty response body)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiEntitiesIdGet()`

```php
apiEntitiesIdGet($id): \OpenAPI\Client\Model\EntityJsonldEntityReadEntityReadParent
```

Retrieves a entity resource.

Retrieves a entity resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: access_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\EntityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | entity identifier

try {
    $result = $apiInstance->apiEntitiesIdGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EntityApi->apiEntitiesIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| entity identifier | |

### Return type

[**\OpenAPI\Client\Model\EntityJsonldEntityReadEntityReadParent**](../Model/EntityJsonldEntityReadEntityReadParent.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/ld+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiEntitiesIdPatch()`

```php
apiEntitiesIdPatch($id, $entity_entity_update): \OpenAPI\Client\Model\EntityJsonldEntityReadEntityReadParent
```

Updates the entity resource.

Updates the entity resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: access_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\EntityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | entity identifier
$entity_entity_update = new \OpenAPI\Client\Model\EntityEntityUpdate(); // \OpenAPI\Client\Model\EntityEntityUpdate | The updated entity resource

try {
    $result = $apiInstance->apiEntitiesIdPatch($id, $entity_entity_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EntityApi->apiEntitiesIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| entity identifier | |
| **entity_entity_update** | [**\OpenAPI\Client\Model\EntityEntityUpdate**](../Model/EntityEntityUpdate.md)| The updated entity resource | |

### Return type

[**\OpenAPI\Client\Model\EntityJsonldEntityReadEntityReadParent**](../Model/EntityJsonldEntityReadEntityReadParent.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

- **Content-Type**: `application/merge-patch+json`
- **Accept**: `application/ld+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiEntitiesPost()`

```php
apiEntitiesPost($entity_jsonld_entity_create): \OpenAPI\Client\Model\EntityJsonldEntityReadEntityReadParent
```

Creates a entity resource.

Creates a entity resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: access_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\EntityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$entity_jsonld_entity_create = new \OpenAPI\Client\Model\EntityJsonldEntityCreate(); // \OpenAPI\Client\Model\EntityJsonldEntityCreate | The new entity resource

try {
    $result = $apiInstance->apiEntitiesPost($entity_jsonld_entity_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EntityApi->apiEntitiesPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **entity_jsonld_entity_create** | [**\OpenAPI\Client\Model\EntityJsonldEntityCreate**](../Model/EntityJsonldEntityCreate.md)| The new entity resource | |

### Return type

[**\OpenAPI\Client\Model\EntityJsonldEntityReadEntityReadParent**](../Model/EntityJsonldEntityReadEntityReadParent.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

- **Content-Type**: `application/ld+json`, `application/json`
- **Accept**: `application/ld+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
