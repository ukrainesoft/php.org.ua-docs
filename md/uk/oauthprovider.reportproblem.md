---
navigation:
  - oauthprovider.removerequiredparameter.md: '« OAuthProvider::removeRequiredParameter'
  - oauthprovider.setparam.md: 'OAuthProvider::setParam »'
  - index.md: PHP Manual
  - class.oauthprovider.md: OAuthProvider
title: 'OAuthProvider::reportProblem'
---
# OAuthProvider::reportProblem

(PECL OAuth >= 1.0.0)

OAuthProvider::reportProblem — Повідомити про проблему

### Опис

```methodsynopsis
final public static OAuthProvider::reportProblem(string $oauthexception, bool $send_headers = true): string
```

Передати проблему як виняток [OAuthException](class.oauthexception.md). Допустимі проблеми перераховані в секції [константи OAuth](oauth.constants.md)

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`oauthexception`

Об'єкт виключення [OAuthException](class.oauthexception.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [OAuthProvider::checkOAuthRequest()](oauthprovider.checkoauthrequest.md) - Перевірка запиту oauth
-   [OAuthProvider::isRequestTokenEndpoint()](oauthprovider.isrequesttokenendpoint.md) - Установка isRequestTokenEndpoint
