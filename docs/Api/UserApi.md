# OpenAPI\Client\UserApi

All URIs are relative to http://localhost:8000, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiUsersIdDelete()**](UserApi.md#apiUsersIdDelete) | **DELETE** /api/users/{id} | Removes the user resource. |
| [**apiUsersIdPatch()**](UserApi.md#apiUsersIdPatch) | **PATCH** /api/users/{id} | Updates the user resource. |
| [**apiUsersPost()**](UserApi.md#apiUsersPost) | **POST** /api/users | Creates a user resource. |
| [**apiUsersresendActivationPost()**](UserApi.md#apiUsersresendActivationPost) | **POST** /api/users/resend-activation | Resend activation email |
| [**apiUsersresetPasswordPost()**](UserApi.md#apiUsersresetPasswordPost) | **POST** /api/users/reset-password | Reset password (with token) |
| [**apiUserssendResetPasswordPost()**](UserApi.md#apiUserssendResetPasswordPost) | **POST** /api/users/send-reset-password | Send reset password email |


## `apiUsersIdDelete()`

```php
apiUsersIdDelete($id)
```

Removes the user resource.

Removes the user resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: access_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | user identifier

try {
    $apiInstance->apiUsersIdDelete($id);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->apiUsersIdDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| user identifier | |

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

## `apiUsersIdPatch()`

```php
apiUsersIdPatch($id, $user_user_update): \OpenAPI\Client\Model\UserJsonldUserEmpty
```

Updates the user resource.

Updates the user resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: access_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | user identifier
$user_user_update = new \OpenAPI\Client\Model\UserUserUpdate(); // \OpenAPI\Client\Model\UserUserUpdate | The updated user resource

try {
    $result = $apiInstance->apiUsersIdPatch($id, $user_user_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->apiUsersIdPatch: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| user identifier | |
| **user_user_update** | [**\OpenAPI\Client\Model\UserUserUpdate**](../Model/UserUserUpdate.md)| The updated user resource | |

### Return type

[**\OpenAPI\Client\Model\UserJsonldUserEmpty**](../Model/UserJsonldUserEmpty.md)

### Authorization

[access_token](../../README.md#access_token)

### HTTP request headers

- **Content-Type**: `application/merge-patch+json`
- **Accept**: `application/ld+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiUsersPost()`

```php
apiUsersPost($user_jsonld_user_create): \OpenAPI\Client\Model\UserJsonldUserEmpty
```

Creates a user resource.

Creates a user resource.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$user_jsonld_user_create = new \OpenAPI\Client\Model\UserJsonldUserCreate(); // \OpenAPI\Client\Model\UserJsonldUserCreate | The new user resource

try {
    $result = $apiInstance->apiUsersPost($user_jsonld_user_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->apiUsersPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_jsonld_user_create** | [**\OpenAPI\Client\Model\UserJsonldUserCreate**](../Model/UserJsonldUserCreate.md)| The new user resource | |

### Return type

[**\OpenAPI\Client\Model\UserJsonldUserEmpty**](../Model/UserJsonldUserEmpty.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/ld+json`, `application/json`
- **Accept**: `application/ld+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiUsersresendActivationPost()`

```php
apiUsersresendActivationPost($user_jsonld_user_resend_activation): \OpenAPI\Client\Model\UserJsonld
```

Resend activation email

This endpoint resends the activation email to the user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$user_jsonld_user_resend_activation = new \OpenAPI\Client\Model\UserJsonldUserResendActivation(); // \OpenAPI\Client\Model\UserJsonldUserResendActivation | The new user resource

try {
    $result = $apiInstance->apiUsersresendActivationPost($user_jsonld_user_resend_activation);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->apiUsersresendActivationPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_jsonld_user_resend_activation** | [**\OpenAPI\Client\Model\UserJsonldUserResendActivation**](../Model/UserJsonldUserResendActivation.md)| The new user resource | |

### Return type

[**\OpenAPI\Client\Model\UserJsonld**](../Model/UserJsonld.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/ld+json`, `application/json`
- **Accept**: `application/ld+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiUsersresetPasswordPost()`

```php
apiUsersresetPasswordPost($user_jsonld_user_reset_password): \OpenAPI\Client\Model\UserJsonldUserEmpty
```

Reset password (with token)

This endpoint resets the password of the user using the token sent by email.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$user_jsonld_user_reset_password = new \OpenAPI\Client\Model\UserJsonldUserResetPassword(); // \OpenAPI\Client\Model\UserJsonldUserResetPassword | The new user resource

try {
    $result = $apiInstance->apiUsersresetPasswordPost($user_jsonld_user_reset_password);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->apiUsersresetPasswordPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_jsonld_user_reset_password** | [**\OpenAPI\Client\Model\UserJsonldUserResetPassword**](../Model/UserJsonldUserResetPassword.md)| The new user resource | |

### Return type

[**\OpenAPI\Client\Model\UserJsonldUserEmpty**](../Model/UserJsonldUserEmpty.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/ld+json`, `application/json`
- **Accept**: `application/ld+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `apiUserssendResetPasswordPost()`

```php
apiUserssendResetPasswordPost($user_jsonld_user_send_reset_password): \OpenAPI\Client\Model\UserJsonldUserEmpty
```

Send reset password email

This endpoint sends a reset password email to the user.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$user_jsonld_user_send_reset_password = new \OpenAPI\Client\Model\UserJsonldUserSendResetPassword(); // \OpenAPI\Client\Model\UserJsonldUserSendResetPassword | The new user resource

try {
    $result = $apiInstance->apiUserssendResetPasswordPost($user_jsonld_user_send_reset_password);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->apiUserssendResetPasswordPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_jsonld_user_send_reset_password** | [**\OpenAPI\Client\Model\UserJsonldUserSendResetPassword**](../Model/UserJsonldUserSendResetPassword.md)| The new user resource | |

### Return type

[**\OpenAPI\Client\Model\UserJsonldUserEmpty**](../Model/UserJsonldUserEmpty.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/ld+json`, `application/json`
- **Accept**: `application/ld+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
