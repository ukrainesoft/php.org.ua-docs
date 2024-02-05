---
navigation:
  - oauthprovider.construct.md: '« OAuthProvider::\_\_construct'
  - oauthprovider.generatetoken.md: 'OAuthProvider::generateToken »'
  - index.md: PHP Manual
  - class.oauthprovider.md: OAuthProvider
title: 'OAuthProvider::consumerHandler'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OAuthProvider::consumerHandler

(PECL OAuth >= 1.0.0)

OAuthProvider::consumerHandler — Встановити обробник consumerHandler

### Опис

```methodsynopsis
public OAuthProvider::consumerHandler(callable $callback_function): void
```

Задає callback-функцію обробника, яка надалі викликатиметься [OAuthProvider::callConsumerHandler()](oauthprovider.callconsumerhandler.md)

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`callback_function`

Функция типа[callable](language.types.callable.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**OAuthProvider::consumerHandler()\*\*\*\*

```php
<?php
function lookupConsumer($provider) {

    if ($provider->consumer_key === 'unknown') {
        return OAUTH_CONSUMER_KEY_UNKNOWN;
    } else if($provider->consumer_key == 'blacklisted' || $provider->consumer_key === 'throttled') {
        return OAUTH_CONSUMER_KEY_REFUSED;
    }

    $provider->consumer_secret = "the_consumers_secret";

    return OAUTH_OK;
}
?>
```

### Дивіться також

-   [OAuthProvider::callConsumerHandler()](oauthprovider.callconsumerhandler.md) \- Викликати callback-функцію consumerNonceHandler
