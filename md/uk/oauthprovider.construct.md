---
navigation:
  - oauthprovider.checkoauthrequest.md: '« OAuthProvider::checkOAuthRequest'
  - oauthprovider.consumerhandler.md: 'OAuthProvider::consumerHandler »'
  - index.md: PHP Manual
  - class.oauthprovider.md: OAuthProvider
title: 'OAuthProvider::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OAuthProvider::\_\_construct

(PECL OAuth >= 1.0.0)

OAuthProvider::\_\_construct - Конструктор класу OAuthProvider

### Опис

```methodsynopsis
public OAuthProvider::__construct(array $params_array = ?)
```

Створює об'єкт класу [OAuthProvider](class.oauthprovider.md)

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`params_array`

Встановлення цих необов'язкових параметрів обмежено [CLI SAPI](features.commandline.md)

### Значення, що повертаються

Об'єкт класу [OAuthProvider](class.oauthprovider.md)

### Приклади

**Пример #1 Пример использования**OAuthProvider::\_\_construct()\*\*\*\*

```php
<?php
try {

    $op = new OAuthProvider();

    // Используем пользовательские callback-функции
    $op->consumerHandler(array($this, 'lookupConsumer'));
    $op->timestampNonceHandler(array($this, 'timestampNonceChecker'));
    $op->tokenHandler(array($this, 'myTokenHandler'));

    // Игнорируем параметр foo_uri
    $op->setParam('foo_uri', NULL);

    // Для данной конечной точки токен не нужен
    $op->setRequestTokenPath('/v1/oauth/request_token');

    $op->checkOAuthRequest();

} catch (OAuthException $e) {

    echo OAuthProvider::reportProblem($e);
}
?>
```

### Дивіться також

-   [OAuthProvider::setParam()](oauthprovider.setparam.md) \- Встановити параметр
