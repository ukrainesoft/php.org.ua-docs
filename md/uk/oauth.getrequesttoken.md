Витягти токен запиту

-   [« OAuth::getRequestHeader](oauth.getrequestheader.html)
    
-   [OAuth::setAuthType »](oauth.setauthtype.html)
    
-   [PHP Manual](index.html)
    
-   [OAuth](class.oauth.html)
    
-   Витягти токен запиту
    

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

HTTP-метод, наприклад `GET` або `POST`

### Значення, що повертаються

Повертає масив обробленого запиту OAuth або **`false`**

### список змін

| Версия            | Описание                                                                   |
|-------------------|----------------------------------------------------------------------------|
| PECL oauth 1.0.0  | Раніше у разі виникнення помилки повертався **`null`** замість **`false`** |
| PECL oauth 0.99.9 | Доданий параметр `callback_url`                                            |

### Приклади

**Приклад #1 Приклад використання **OAuth::getRequestToken()****

```php
<?php
try {
    $oauth = new OAuth(OAUTH_CONSUMER_KEY,OAUTH_CONSUMER_SECRET);
    $request_token_info = $oauth->getRequestToken("https://example.com/oauth/request_token");
    if(!empty($request_token_info)) {
        print_r($request_token_info);
    } else {
        print "Не удалось получить токен доступа, ответ был: " . $oauth->getLastResponse();
    }
} catch(OAuthException $E) {
    echo "Ответ: ". $E->lastResponse . "\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [oauth_token] => some_token
    [oauth_token_secret] => some_token_secret
)
```

### Дивіться також

-   [OAuth::getLastResponse()](oauth.getlastresponse.html) - Отримати останню відповідь
-   [OAuth::getLastResponseInfo()](oauth.getlastresponseinfo.html) - Отримати HTTP-інформацію про останню відповідь