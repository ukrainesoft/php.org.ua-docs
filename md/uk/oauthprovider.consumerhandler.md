Встановити обробник consumerHandler

-   [« OAuthProvider::\_\_construct](oauthprovider.construct.html)
    
-   [OAuthProvider::generateToken »](oauthprovider.generatetoken.html)
    
-   [PHP Manual](index.html)
    
-   [OAuthProvider](class.oauthprovider.html)
    
-   Встановити обробник consumerHandler
    

# OAuthProvider::consumerHandler

(PECL OAuth >= 1.0.0)

OAuthProvider::consumerHandler — Встановити обробник consumerHandler

### Опис

```methodsynopsis
public OAuthProvider::consumerHandler(callable $callback_function): void
```

Задає callback-функцію обробника, яка надалі викликатиметься [OAuthProvider::callConsumerHandler()](oauthprovider.callconsumerhandler.html)

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`callback_function`

Функція типу [callable](language.types.callable.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **OAuthProvider::consumerHandler()****

```php
<?php
function lookupConsumer($provider) {

    if ($provider->consumer_key === 'unknown') {
        return OAUTH_CONSUMER_KEY_UNKNOWN;
    } else if($provider->consumer_key == 'blacklisted' || $provider->consumer_key === 'throttled') {
        return OAUTH_CONSUMER_KEY_REFUSED;
    }

    $provider->consumer_secret = "the_consumers_secret";

    return OAUTH_OK;
}
?>
```

### Дивіться також

-   [OAuthProvider::callConsumerHandler()](oauthprovider.callconsumerhandler.html) - Викликати callback-функцію consumerNonceHandler