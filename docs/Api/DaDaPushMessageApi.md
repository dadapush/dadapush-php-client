# DaDaPushClient\DaDaPushMessageApi

All URIs are relative to *https://www.dadapush.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createMessage**](DaDaPushMessageApi.md#createMessage) | **POST** /api/v1/message | push Message to a Channel
[**deleteMessage**](DaDaPushMessageApi.md#deleteMessage) | **DELETE** /api/v1/message/{messageId} | delete a Channel Message
[**getMessage**](DaDaPushMessageApi.md#getMessage) | **GET** /api/v1/message/{messageId} | get a Channel Message
[**getMessages**](DaDaPushMessageApi.md#getMessages) | **GET** /api/v1/messages | get Message List



## createMessage

> \DaDaPushClient\Model\ResultOfMessagePushResponse createMessage($body, $x_channel_token)

push Message to a Channel

<h2>Rate Limit:</h2><ul><li>1 request per 1s</li><li>30 request per 1m</li><li>500 request per 1h</li></ul><h2>Result code/errmsg List:</h2><ul><li>0: ok</li><li>1: server error</li><li>101: channel is exists</li><li>102: channel is not exists</li><li>103: channel token error</li><li>104: channel is not exists</li><li>105: message is not exists</li><li>204: bad request</li><li>205: permission deny</li><li>206: too many request, please after 5 minutes to try!</li><li>301: duplicate username/email</li><li>302: user is not exists</li><li>303: user password is error</li><li>304: client push token is error</li><li>305: user is disabled</li><li>306: your subscription is expired</li><li>307: user not subscribe channel</li></ul>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new DaDaPushClient\Api\DaDaPushMessageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \DaDaPushClient\Model\MessagePushRequest(); // \DaDaPushClient\Model\MessagePushRequest | body
$x_channel_token = 'x_channel_token_example'; // string | see: https://www.dadapush.com/channel/list

try {
    $result = $apiInstance->createMessage($body, $x_channel_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DaDaPushMessageApi->createMessage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\DaDaPushClient\Model\MessagePushRequest**](../Model/MessagePushRequest.md)| body |
 **x_channel_token** | **string**| see: https://www.dadapush.com/channel/list | [optional]

### Return type

[**\DaDaPushClient\Model\ResultOfMessagePushResponse**](../Model/ResultOfMessagePushResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## deleteMessage

> \DaDaPushClient\Model\Result deleteMessage($message_id, $x_channel_token)

delete a Channel Message

<h2>Rate Limit:</h2><ul><li>10 request per 1s</li><li>100 request per 1m</li><li>1000 request per 1h</li></ul><h2>Result code/errmsg List:</h2><ul><li>0: ok</li><li>1: server error</li><li>101: channel is exists</li><li>102: channel is not exists</li><li>103: channel token error</li><li>104: channel is not exists</li><li>105: message is not exists</li><li>204: bad request</li><li>205: permission deny</li><li>206: too many request, please after 5 minutes to try!</li><li>301: duplicate username/email</li><li>302: user is not exists</li><li>303: user password is error</li><li>304: client push token is error</li><li>305: user is disabled</li><li>306: your subscription is expired</li><li>307: user not subscribe channel</li></ul>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new DaDaPushClient\Api\DaDaPushMessageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$message_id = 56; // int | messageId
$x_channel_token = 'x_channel_token_example'; // string | see: https://www.dadapush.com/channel/list

try {
    $result = $apiInstance->deleteMessage($message_id, $x_channel_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DaDaPushMessageApi->deleteMessage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **message_id** | **int**| messageId |
 **x_channel_token** | **string**| see: https://www.dadapush.com/channel/list | [optional]

### Return type

[**\DaDaPushClient\Model\Result**](../Model/Result.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## getMessage

> \DaDaPushClient\Model\ResultOfMessageObject getMessage($message_id, $x_channel_token)

get a Channel Message

<h2>Rate Limit:</h2><ul><li>10 request per 1s</li><li>100 request per 1m</li><li>1000 request per 1h</li></ul><h2>Result code/errmsg List:</h2><ul><li>0: ok</li><li>1: server error</li><li>101: channel is exists</li><li>102: channel is not exists</li><li>103: channel token error</li><li>104: channel is not exists</li><li>105: message is not exists</li><li>204: bad request</li><li>205: permission deny</li><li>206: too many request, please after 5 minutes to try!</li><li>301: duplicate username/email</li><li>302: user is not exists</li><li>303: user password is error</li><li>304: client push token is error</li><li>305: user is disabled</li><li>306: your subscription is expired</li><li>307: user not subscribe channel</li></ul>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new DaDaPushClient\Api\DaDaPushMessageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$message_id = 56; // int | messageId
$x_channel_token = 'x_channel_token_example'; // string | see: https://www.dadapush.com/channel/list

try {
    $result = $apiInstance->getMessage($message_id, $x_channel_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DaDaPushMessageApi->getMessage: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **message_id** | **int**| messageId |
 **x_channel_token** | **string**| see: https://www.dadapush.com/channel/list | [optional]

### Return type

[**\DaDaPushClient\Model\ResultOfMessageObject**](../Model/ResultOfMessageObject.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## getMessages

> \DaDaPushClient\Model\ResultOfPageResponseOfMessageObject getMessages($page, $page_size, $x_channel_token)

get Message List

<h2>Rate Limit:</h2><ul><li>1 request per 1s</li><li>45 request per 1m</li></ul><h2>Result code/errmsg List:</h2><ul><li>0: ok</li><li>1: server error</li><li>101: channel is exists</li><li>102: channel is not exists</li><li>103: channel token error</li><li>104: channel is not exists</li><li>105: message is not exists</li><li>204: bad request</li><li>205: permission deny</li><li>206: too many request, please after 5 minutes to try!</li><li>301: duplicate username/email</li><li>302: user is not exists</li><li>303: user password is error</li><li>304: client push token is error</li><li>305: user is disabled</li><li>306: your subscription is expired</li><li>307: user not subscribe channel</li></ul>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new DaDaPushClient\Api\DaDaPushMessageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$page = 1; // int | greater than 1
$page_size = 10; // int | range is 1,50
$x_channel_token = 'x_channel_token_example'; // string | see: https://www.dadapush.com/channel/list

try {
    $result = $apiInstance->getMessages($page, $page_size, $x_channel_token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DaDaPushMessageApi->getMessages: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**| greater than 1 | [default to 1]
 **page_size** | **int**| range is 1,50 | [default to 10]
 **x_channel_token** | **string**| see: https://www.dadapush.com/channel/list | [optional]

### Return type

[**\DaDaPushClient\Model\ResultOfPageResponseOfMessageObject**](../Model/ResultOfPageResponseOfMessageObject.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)

