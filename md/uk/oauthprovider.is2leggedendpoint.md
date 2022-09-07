---
navigation:
  - oauthprovider.generatetoken.md: '« OAuthProvider::generateToken'
  - oauthprovider.isrequesttokenendpoint.md: 'OAuthProvider::isRequestTokenEndpoint »'
  - index.md: PHP Manual
  - class.oauthprovider.md: OAuthProvider
title: 'OAuthProvider::is2LeggedEndpoint'
---
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

Об'єкт [OAuthProvider](class.oauthprovider.md)

### Приклади

**Приклад #1 Приклад використання **OAuthProvider::is2LeggedEndpoint()****

```php
<?php

$provider = new OAuthProvider();

$provider->is2LeggedEndpoint(true);

?>
```

### Дивіться також

-   [OAuthProvider::construct()](oauthprovider.construct.md) - Конструктор класу OAuthProvider
