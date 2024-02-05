---
navigation:
  - oauthprovider.generatetoken.md: '« OAuthProvider::generateToken'
  - oauthprovider.isrequesttokenendpoint.md: 'OAuthProvider::isRequestTokenEndpoint »'
  - index.md: PHP Manual
  - class.oauthprovider.md: OAuthProvider
title: 'OAuthProvider::is2LeggedEndpoint'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`params_array`

### Значення, що повертаються

Об'єкт [OAuthProvider](class.oauthprovider.md)

### Приклади

**Пример #1 Пример использования**OAuthProvider::is2LeggedEndpoint()\*\*\*\*

```php
<?php

$provider = new OAuthProvider();

$provider->is2LeggedEndpoint(true);

?>
```

### Дивіться також

-   [OAuthProvider::\_\_construct()](oauthprovider.construct.md) \- Конструктор класу OAuthProvider
