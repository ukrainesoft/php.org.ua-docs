---
navigation:
  - oauthprovider.setrequesttokenpath.md: '« OAuthProvider::setRequestTokenPath'
  - oauthprovider.tokenhandler.md: 'OAuthProvider::tokenHandler »'
  - index.md: PHP Manual
  - class.oauthprovider.md: OAuthProvider
title: 'OAuthProvider::timestampNonceHandler'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OAuthProvider::timestampNonceHandler

(PECL OAuth >= 1.0.0)

OAuthProvider::timestampNonceHandler — Встановити обробник timestampNonceHandler

### Опис

```methodsynopsis
public OAuthProvider::timestampNonceHandler(callable $callback_function): void
```

Встановлює callback-функцію, що використовується в [OAuthProvider::callTimestampNonceHandler()](oauthprovider.calltimestampnoncehandler.md). У цей обробник будуть передані помилки, що стосуються timestamp/nonce.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`callback_function`

Функция типа[callable](language.types.callable.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** OAuthProvider::timestampNonceHandler()\*\*\*\*

```php
<?php
function timestampNonceChecker($provider) {

    if ($provider->nonce === 'bad') {
        return OAUTH_BAD_NONCE;
    } elseif ($provider->timestamp == '0') {
        return OAUTH_BAD_TIMESTAMP;
    }

    return OAUTH_OK;
}
?>
```

### Дивіться також

-   [OAuthProvider::callTimestampNonceHandler()](oauthprovider.calltimestampnoncehandler.md) \- Викликати callback-функцію timestampNonceHandler
