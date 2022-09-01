---
navigation:
  - oauthprovider.checkoauthrequest.html: '« OAuthProvider::checkOAuthRequest'
  - oauthprovider.consumerhandler.html: 'OAuthProvider::consumerHandler »'
  - index.html: PHP Manual
  - class.oauthprovider.html: OAuthProvider
title: 'OAuthProvider::construct'
---
# OAuthProvider::construct

(PECL OAuth >= 1.0.0)

OAuthProvider::construct - Конструктор класу OAuthProvider

### Опис

```methodsynopsis
public OAuthProvider::__construct(array $params_array = ?)
```

Створює об'єкт класу [OAuthProvider](class.oauthprovider.html)

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`params_array`

Встановлення цих необов'язкових параметрів обмежено [CLI SAPI](features.commandline.html)

### Значення, що повертаються

Об'єкт класу [OAuthProvider](class.oauthprovider.html)

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

-   [OAuthProvider::setParam()](oauthprovider.setparam.html) - Встановити параметр
