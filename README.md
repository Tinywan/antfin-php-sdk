
<h1 align="center">:moneybag: 蚂蚁金服PHP-SDK</h1>

<p align="center">蚂蚁金服PHP-SDK</p>

[![Build Status](https://travis-ci.org/Tinywan/weather.svg?branch=master)](https://travis-ci.org/tinywan/weather)

## 安装

```sh
composer require tinywan/antfin-php-sdk -vvv
```

## 使用

```php
use AntCloudSDKCore\AntCloudClient;

// 初始化客户端
$client = new AntCloudClient(
    "https://prodapigw.cloud.alipay.com/gateway.do",
    "<your-access-key>",
    "<your-access-secret>"
);

// 构建请求
$request = array(
    "cert_id" => "0001",
    "org_did" => "dimychain:66530b21a9bee783234c442b653e909136629a5a3075be7b4d9ae085782e3d36",
    "method" => "baas.ebc.cert.query",
    "version" => "1.0",
    "product_instance_id" => "7304XXXXXXXX",
    "region_name" => "CN-HANGZHOU-FINANCE",
);

// 发送调用请求，解析响应结果
$response = $client->execute($request);
```