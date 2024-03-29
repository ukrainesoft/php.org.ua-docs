---
navigation:
  - oauth.enablesslchecks.md: '« OAuth::enableSSLChecks'
  - oauth.generatesignature.md: 'OAuth::generateSignature »'
  - index.md: PHP Manual
  - class.oauth.md: OAuth
title: 'OAuth::fetch'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OAuth::fetch

(PECL OAuth >= 0.99.1)

OAuth::fetch — Витягти захищений ресурс OAuth

### Опис

```methodsynopsis
public OAuth::fetch(    string $protected_resource_url,    array $extra_parameters = ?,    string $http_method = ?,    array $http_headers = ?): mixed
```

Витягти ресурс.

### Список параметрів

`protected_resource_url`

URL захищеного ресурсу OAuth.

`extra_parameters`

Додаткові опції запиту ресурсу.

`http_method`

Один из методов\*\*`OAUTH_HTTP_METHOD_*`\*\*Смотрите[константи OAUTH](oauth.constants.md)які включають GET, POST, PUT, HEAD і DELETE.

HEAD (**`OAUTH_HTTP_METHOD_HEAD`**) може бути корисним для вивчення інформації перед твором запиту (якщо облікові дані OAuth у заголовку `Authorization`

`http_headers`

Клієнтські заголовки HTTP (такі як User-Agent, Accept тощо)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| PECL oauth 1.0.0 | Раніше у разі виникнення помилки повертався **`null`** замість **`false`** |
| PECL oauth 0.99.5 | Добавлен параметр`http_method` |
| PECL oauth 0.99.8 | Добавлен параметр`http_headers` |

### Приклади

**Приклад #1 Приклад використання** OAuth::fetch()\*\*\*\*

```php
<?php
try {
    $oauth = new OAuth("consumer_key","consumer_secret",OAUTH_SIG_METHOD_HMACSHA1,OAUTH_AUTH_TYPE_AUTHORIZATION);
    $oauth->setToken("access_token","access_token_secret");

    $oauth->fetch("http://photos.example.net/photo?file=vacation.jpg");

    $response_info = $oauth->getLastResponseInfo();
    header("Content-Type: {$response_info["content_type"]}");
    echo $oauth->getLastResponse();
} catch(OAuthException $E) {
    echo "Поймали исключение!\n";
    echo "Ответ: ". $E->lastResponse . "\n";
}
?>
```

### Дивіться також

-   [OAuth::getLastResponse()](oauth.getlastresponse.md) \- Отримати останню відповідь
-   [OAuth::getLastResponseInfo()](oauth.getlastresponseinfo.md) \- Отримати HTTP-інформацію про останню відповідь
-   [OAuth::setToken()](oauth.settoken.md) \- Задати токен та його пароль
