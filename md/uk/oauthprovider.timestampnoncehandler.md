Встановити обробник timestampNonceHandler

-   [« OAuthProvider::setRequestTokenPath](oauthprovider.setrequesttokenpath.html)
    
-   [OAuthProvider::tokenHandler »](oauthprovider.tokenhandler.html)
    
-   [PHP Manual](index.html)
    
-   [OAuthProvider](class.oauthprovider.html)
    
-   Встановити обробник timestampNonceHandler
    

# OAuthProvider::timestampNonceHandler

(PECL OAuth >= 1.0.0)

OAuthProvider::timestampNonceHandler — Встановити обробник timestampNonceHandler

### Опис

```methodsynopsis
public OAuthProvider::timestampNonceHandler(callable $callback_function): void
```

Встановлює callback-функцію, що використовується в [OAuthProvider::callTimestampNonceHandler()](oauthprovider.calltimestampnoncehandler.html). У цей обробник будуть передані помилки, що стосуються timestamp/nonce.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`callback_function`

Функція типу [callable](language.types.callable.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **OAuthProvider::timestampNonceHandler()****

```php
<?php
function timestampNonceChecker($provider) {

    if ($provider->nonce === 'bad') {
        return OAUTH_BAD_NONCE;
    } elseif ($provider->timestamp == '0') {
        return OAUTH_BAD_TIMESTAMP;
    }

    return OAUTH_OK;
}
?>
```

### Дивіться також

-   [OAuthProvider::callTimestampNonceHandler()](oauthprovider.calltimestampnoncehandler.html) - Викликати callback-функцію timestampNonceHandler