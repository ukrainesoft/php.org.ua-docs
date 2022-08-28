Задати токен та його пароль

-   [« OAuth::setTimestamp](oauth.settimestamp.html)
    
-   [OAuth::setVersion »](oauth.setversion.html)
    
-   [PHP Manual](index.html)
    
-   [OAuth](class.oauth.html)
    
-   Задати токен та його пароль
    

# OAuth::setToken

(PECL OAuth >= 0.99.1)

OAuth::setToken — Задати токен та його пароль

### Опис

```methodsynopsis
public OAuth::setToken(string $token, string $token_secret): bool
```

Встановлює токен та його пароль для наступних запитів.

### Список параметрів

`token`

Токен OAuth.

`token_secret`

Пароль токена OAuth.

### Значення, що повертаються

**`true`**

### Приклади

**Приклад #1 Приклад використання **OAuth::setToken()****

```php
<?php
$oauth = new OAuth(OAUTH_CONSUMER_KEY,OAUTH_CONSUMER_SECRET);
$oauth->setToken("token","token-secret");
?>
```