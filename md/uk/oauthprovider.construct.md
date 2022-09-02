---
navigation:
  - oauthprovider.checkoauthrequest.md: '« OAuthProvider::checkOAuthRequest'
  - oauthprovider.consumerhandler.md: 'OAuthProvider::consumerHandler »'
  - index.md: PHP Manual
  - class.oauthprovider.md: OAuthProvider
title: 'OAuthProvider::construct'
---
# OAuthProvider::construct

(PECL OAuth >= 1.0.0)

OAuthProvider::construct - Конструктор класу OAuthProvider

### Опис

```methodsynopsis
public OAuthProvider::__construct(array $params_array = ?)
```

Створює об'єкт класу [OAuthProvider](class.oauthprovider.md)

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`params_array`

Встановлення цих необов'язкових параметрів обмежено [CLI SAPI](features.commandline.md)

### Значення, що повертаються

Об'єкт класу [OAuthProvider](class.oauthprovider.md)

### Приклади

**Приклад #1 Приклад використання **OAuthProvider::construct()****

```php
<?php
try {

    $op = new OAuthProvider();

    // Используем пользовательские callback-функции
    $op->consumerHandler(array($this, 'lookupConsumer'));
    $op->timestampNonceHandler(array($this, 'timestampNonceChecker'));
    $op->tokenHandler(array($this, 'myTokenHandler'));

    // Игнорируем параметр foo_uri
    $op->setParam('foo_uri', NULL);

    // Для данной конечной точки токен не нужен
    $op->setRequestTokenPath('/v1/oauth/request_token');

    $op->checkOAuthRequest();

} catch (OAuthException $e) {

    echo OAuthProvider::reportProblem($e);
}
?>
```

### Дивіться також

-   [OAuthProvider::setParam()](oauthprovider.setparam.md) - Встановити параметр
