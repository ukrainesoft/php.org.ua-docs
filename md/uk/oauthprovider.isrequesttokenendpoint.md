---
navigation:
  - oauthprovider.is2leggedendpoint.md: '« OAuthProvider::is2LeggedEndpoint'
  - oauthprovider.removerequiredparameter.md: 'OAuthProvider::removeRequiredParameter »'
  - index.md: PHP Manual
  - class.oauthprovider.md: OAuthProvider
title: 'OAuthProvider::isRequestTokenEndpoint'
---
# OAuthProvider::isRequestTokenEndpoint

(PECL OAuth >= 1.0.0)

OAuthProvider::isRequestTokenEndpoint — Установка isRequestTokenEndpoint

### Опис

```methodsynopsis
public OAuthProvider::isRequestTokenEndpoint(bool $will_issue_request_token): void
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`will_issue_request_token`

Встановлює, чи видаватиме токен запиту, тим самим визначаючи, чи потрібно викликати [OAuthProvider::tokenHandler()](oauthprovider.tokenhandler.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [OAuthProvider::setRequestTokenPath()](oauthprovider.setrequesttokenpath.md) - Встановити шлях запиту токена
-   [OAuthProvider::reportProblem()](oauthprovider.reportproblem.md) - Повідомити про проблему
