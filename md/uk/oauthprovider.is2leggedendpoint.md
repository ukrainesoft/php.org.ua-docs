is2LeggedEndpoint

-   [« OAuthProvider::generateToken](oauthprovider.generatetoken.html)
    
-   [OAuthProvider::isRequestTokenEndpoint »](oauthprovider.isrequesttokenendpoint.html)
    
-   [PHP Manual](index.html)
    
-   [OAuthProvider](class.oauthprovider.html)
    
-   is2LeggedEndpoint
    

# OAuthProvider::is2LeggedEndpoint

(PECL OAuth >= 1.0.0)

OAuthProvider::is2LeggedEndpoint — is2LeggedEndpoint

### Опис

```methodsynopsis
public OAuthProvider::is2LeggedEndpoint(mixed $params_array): void
```

Двосторонній потік або запит підпису. Не потребує токена.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`params_array`

### Значення, що повертаються

Об'єкт [OAuthProvider](class.oauthprovider.html)

### Приклади

**Приклад #1 Приклад використання **OAuthProvider::is2LeggedEndpoint()****

```php
<?php

$provider = new OAuthProvider();

$provider->is2LeggedEndpoint(true);

?>
```

### Дивіться також

-   [OAuthProvider::\_\_construct()](oauthprovider.construct.html) - Конструктор класу OAuthProvider