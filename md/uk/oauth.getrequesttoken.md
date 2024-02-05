---
navigation:
  - oauth.getrequestheader.md: '« OAuth::getRequestHeader'
  - oauth.setauthtype.md: 'OAuth::setAuthType »'
  - index.md: PHP Manual
  - class.oauth.md: OAuth
title: 'OAuth::getRequestToken'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OAuth::getRequestToken

(PECL OAuth >= 0.99.1)

OAuth::getRequestToken — Витягти токен запиту

### Опис

```methodsynopsis
public OAuth::getRequestToken(string $request_token_url, string $callback_url = ?, string $http_method = ?): array
```

Отримати токен запиту, його пароль та додаткові параметри відповіді від постачальника послуг.

### Список параметрів

`request_token_url`

URL до API токена запиту.

`callback_url`

URL callback-функції OAuth. Якщо `callback_url` Заданий порожнім значенням, то він встановиться як "oob" рішення OAuth 2009.1.

`http_method`

HTTP-метод, например`GET`или`POST`

### Значення, що повертаються

Повертає масив обробленого запиту OAuth або **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| PECL oauth 1.0.0 | Раніше у разі виникнення помилки повертався **`null`** замість **`false`** |
| PECL oauth 0.99.9 | Добавлен параметр`callback_url` |

### Приклади

**Пример #1 Пример использования**OAuth::getRequestToken()\*\*\*\*

```php
<?php
try {
    $oauth = new OAuth(OAUTH_CONSUMER_KEY,OAUTH_CONSUMER_SECRET);
    $request_token_info = $oauth->getRequestToken("https://example.com/oauth/request_token");
    if(!empty($request_token_info)) {
        print_r($request_token_info);
    } else {
        print "Не удалось получить токен доступа, ответ был: " . $oauth->getLastResponse();
    }
} catch(OAuthException $E) {
    echo "Ответ: ". $E->lastResponse . "\n";
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [oauth_token] => some_token
    [oauth_token_secret] => some_token_secret
)
```

### Дивіться також

-   [OAuth::getLastResponse()](oauth.getlastresponse.md) \- Отримати останню відповідь
-   [OAuth::getLastResponseInfo()](oauth.getlastresponseinfo.md) \- Отримати HTTP-інформацію про останню відповідь
