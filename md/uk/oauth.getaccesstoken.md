---
navigation:
  - oauth.generatesignature.md: '« OAuth::generateSignature'
  - oauth.getcapath.md: 'OAuth::getCAPath »'
  - index.md: PHP Manual
  - class.oauth.md: OAuth
title: 'OAuth::getAccessToken'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OAuth::getAccessToken

(PECL OAuth >= 0.99.1)

OAuth::getAccessToken — Отримати токен доступу

### Опис

```methodsynopsis
public OAuth::getAccessToken(    string $access_token_url,    string $auth_session_handle = ?,    string $verifier_token = ?,    string $http_method = ?): array
```

Отримує токен доступу, його пароль та всі додаткові параметри відповіді від провайдера сервісу.

### Список параметрів

`access_token_url`

URL до API видачі токена доступу.

`auth_session_handle`

Обробник сесії авторизації. Цей параметр не описується в специфікації OAuth 1.0, але безліччю провайдерів реалізується. Детальніше читайте за посиланням [» ScalableOAuth](http://oauth.pbwiki.com/ScalableOAuth/)

`verifier_token`

Для провайдерів із підтримкою 1.0a, параметр `verifier_token` повинен бути заданий під час обміну токена запиту на токен доступу. Якщо `verifier_token` присутній у `$_GET`или`$_POST`, то він буде заданий автоматично і стороні, що викликає, не потрібно явно його задавати в параметрі `verifier_token` (звичайно якщо токен доступу обмінюється за допомогою oauth\_callback URL). Детальніше читайте за посиланням [» ScalableOAuth](http://oauth.pbwiki.com/ScalableOAuth/)

`http_method`

Метод HTTP. НаПриклад`GET`или`POST`

### Значення, що повертаються

Повертає масив із розібраною відповіддю OAuth, або **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| PECL oauth 1.0.0 | Раніше у разі виникнення помилки повертався **`null`** замість **`false`** |
| PECL oauth 0.99.9 | Добавлен параметр`verifier_token` |

### Приклади

**Приклад #1 Приклад використання** OAuth::getAccessToken()\*\*\*\*

```php
<?php
try {
    $oauth = new OAuth(OAUTH_CONSUMER_KEY,OAUTH_CONSUMER_SECRET);
    $oauth->setToken($request_token,$request_token_secret);
    $access_token_info = $oauth->getAccessToken("https://example.com/oauth/access_token");
    if(!empty($access_token_info)) {
        print_r($access_token_info);
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
-   [OAuth::setToken()](oauth.settoken.md) \- Задати токен та його пароль
