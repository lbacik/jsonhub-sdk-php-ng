# OpenAPI\Client\DefinitionApi

All URIs are relative to http://localhost:8000, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiDefinitionsGetCollection()**](DefinitionApi.md#apiDefinitionsGetCollection) | **GET** /api/definitions | Retrieves the collection of definition resources. |
| [**apiDefinitionsIdDelete()**](DefinitionApi.md#apiDefinitionsIdDelete) | **DELETE** /api/definitions/{id} | Removes the definition resource. |
| [**apiDefinitionsIdGet()**](DefinitionApi.md#apiDefinitionsIdGet) | **GET** /api/definitions/{id} | Retrieves a definition resource. |
| [**apiDefinitionsIdPatch()**](DefinitionApi.md#apiDefinitionsIdPatch) | **PATCH** /api/definitions/{id} | Updates the definition resource. |
| [**apiDefinitionsPost()**](DefinitionApi.md#apiDefinitionsPost) | **POST** /api/definitions | Creates a definition resource. |


## `apiDefinitionsGetCollection()`

```php
apiDefinitionsGetCollection($qid, $is_owned_by_me, $page, $limit, $properties, $parent_entity): \OpenAPI\Client\Model\ApiDefinitionsGetCollection200Response
```

Retrieves the collection of definition resources.

Retrieves the collection of definition resources.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: access_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DefinitionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$qid = 'qid_example'; // string | Filter by slug/id (partial match)
$is_owned_by_me = True; // bool | Show only definitions owned by the current user
$page = 1; // int | The collection page number
$limit = 10; // int | The number of items per page
$properties = array('properties_example'); // string[] | Allows you to reduce the response to contain only the properties you need. If your desired property is nested, you can address it using nested arrays. Example: properties[]={propertyName}&properties[]={anotherPropertyName}&properties[{nestedPropertyParent}][]={nestedProperty}
$parent_entity = 'parent_entity_example'; // string | Filter by parentEntity (uuid)

try {
    $result = $apiInstance->apiDefinitionsGetCollection($qid, $is_owned_by_me, $page, $limit, $properties, $parent_entity);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefinitionApi->apiDefinitionsGetCollection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **qid** | **string**| Filter by slug/id (partial match) | [optional] |
| **is_owned_by_me** | **bool**| Show only definitions owned by the current user | [optional] |
| **page** | **int**| The collection page number | [optional] [default to 1] |
| **limit** | **int**| The number of items per page | [optional] [default to 10] |
| **properties** | [**string[]**](../Model/string.md)| Allows you to reduce the response to contain only the properties you need. If your desired property is nested, you can address it using nested arrays. Example: properties[]&#x3D;{propertyName}&amp;properties[]&#x3D;{anotherPropertyName}&amp;properties[{nestedPropertyParent}][]&#x3D;{nestedProperty} | [optional] |
| **parent_entity** | **string**| Filter by parentEntity (uuid) | [optional] |

### Return type

[**\OpenAPI\Client\Model\ApiDefinitionsGetCollection200Response**](../Model/ApiDefinitionsGetCollection200Response.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/ld+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiDefinitionsIdDelete()`

```php
apiDefinitionsIdDelete($id)
```

Removes the definition resource.

Removes the definition resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: access_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DefinitionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | definition identifier

try {
    $apiInstance->apiDefinitionsIdDelete($id);
} catch (Exception $e) {
    echo 'Exception when calling DefinitionApi->apiDefinitionsIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| definition identifier | |

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

## `apiDefinitionsIdGet()`

```php
apiDefinitionsIdGet($id): \OpenAPI\Client\Model\DefinitionJsonldDefinitionRead
```

Retrieves a definition resource.

Retrieves a definition resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: access_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DefinitionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | definition identifier

try {
    $result = $apiInstance->apiDefinitionsIdGet($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefinitionApi->apiDefinitionsIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| definition identifier | |

### Return type

[**\OpenAPI\Client\Model\DefinitionJsonldDefinitionRead**](../Model/DefinitionJsonldDefinitionRead.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/ld+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiDefinitionsIdPatch()`

```php
apiDefinitionsIdPatch($id, $definition_definition_write): \OpenAPI\Client\Model\DefinitionJsonldDefinitionRead
```

Updates the definition resource.

Updates the definition resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: access_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DefinitionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | definition identifier
$definition_definition_write = new \OpenAPI\Client\Model\DefinitionDefinitionWrite(); // \OpenAPI\Client\Model\DefinitionDefinitionWrite | The updated definition resource

try {
    $result = $apiInstance->apiDefinitionsIdPatch($id, $definition_definition_write);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefinitionApi->apiDefinitionsIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| definition identifier | |
| **definition_definition_write** | [**\OpenAPI\Client\Model\DefinitionDefinitionWrite**](../Model/DefinitionDefinitionWrite.md)| The updated definition resource | |

### Return type

[**\OpenAPI\Client\Model\DefinitionJsonldDefinitionRead**](../Model/DefinitionJsonldDefinitionRead.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

- **Content-Type**: `application/merge-patch+json`
- **Accept**: `application/ld+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiDefinitionsPost()`

```php
apiDefinitionsPost($definition_jsonld_definition_write): \OpenAPI\Client\Model\DefinitionJsonldDefinitionRead
```

Creates a definition resource.

Creates a definition resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: access_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DefinitionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$definition_jsonld_definition_write = new \OpenAPI\Client\Model\DefinitionJsonldDefinitionWrite(); // \OpenAPI\Client\Model\DefinitionJsonldDefinitionWrite | The new definition resource

try {
    $result = $apiInstance->apiDefinitionsPost($definition_jsonld_definition_write);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefinitionApi->apiDefinitionsPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **definition_jsonld_definition_write** | [**\OpenAPI\Client\Model\DefinitionJsonldDefinitionWrite**](../Model/DefinitionJsonldDefinitionWrite.md)| The new definition resource | |

### Return type

[**\OpenAPI\Client\Model\DefinitionJsonldDefinitionRead**](../Model/DefinitionJsonldDefinitionRead.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

- **Content-Type**: `application/ld+json`, `application/json`
- **Accept**: `application/ld+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
