---
navigation:
  - oauthprovider.timestampnoncehandler.md: '« OAuthProvider::timestampNonceHandler'
  - class.oauthexception.md: OAuthException »
  - index.md: PHP Manual
  - class.oauthprovider.md: OAuthProvider
title: 'OAuthProvider::tokenHandler'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OAuthProvider::tokenHandler

(PECL OAuth >= 1.0.0)

OAuthProvider::tokenHandler — Встановити обробник tokenHandler

### Опис

```methodsynopsis
public OAuthProvider::tokenHandler(callable $callback_function): void
```

Встановлює callback-функцію обробника токена, яка використовуватиметься [OAuthProvider::callTokenHandler()](oauthprovider.calltokenhandler.md)

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`callback_function`

Функция типа[callable](language.types.callable.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** OAuthProvider::tokenHandler()\*\*\*\*

```php
<?php
function tokenHandler($provider) {

    if ($provider->token === 'rejected') {
        return OAUTH_TOKEN_REJECTED;
    } elseif ($provider->token === 'revoked') {
        return OAUTH_TOKEN_REVOKED;
    }

    $provider->token_secret = "the_tokens_secret";
    return OAUTH_OK;
}
?>
```

### Дивіться також

-   [OAuthProvider::callTokenHandler()](oauthprovider.calltokenhandler.md) \- Викликати callback-функцію tokenNonceHandler
