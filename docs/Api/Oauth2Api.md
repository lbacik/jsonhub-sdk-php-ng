# OpenAPI\Client\Oauth2Api

All URIs are relative to http://localhost:8000, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiOauth2tokenPost()**](Oauth2Api.md#apiOauth2tokenPost) | **POST** /api/oauth2/token | Retrieve an OAuth2 Token |


## `apiOauth2tokenPost()`

```php
apiOauth2tokenPost($oauth2_jsonld_oauth2_write): \OpenAPI\Client\Model\Oauth2JsonldOauth2Read
```

Retrieve an OAuth2 Token

This endpoint issues an OAuth2 token using your client credentials.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\Oauth2Api(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$oauth2_jsonld_oauth2_write = new \OpenAPI\Client\Model\Oauth2JsonldOauth2Write(); // \OpenAPI\Client\Model\Oauth2JsonldOauth2Write | The new oauth2 resource

try {
    $result = $apiInstance->apiOauth2tokenPost($oauth2_jsonld_oauth2_write);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling Oauth2Api->apiOauth2tokenPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **oauth2_jsonld_oauth2_write** | [**\OpenAPI\Client\Model\Oauth2JsonldOauth2Write**](../Model/Oauth2JsonldOauth2Write.md)| The new oauth2 resource | |

### Return type

[**\OpenAPI\Client\Model\Oauth2JsonldOauth2Read**](../Model/Oauth2JsonldOauth2Read.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/ld+json`, `application/json`
- **Accept**: `application/ld+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
