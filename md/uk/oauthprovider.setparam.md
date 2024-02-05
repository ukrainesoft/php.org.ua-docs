---
navigation:
  - oauthprovider.reportproblem.md: '« OAuthProvider::reportProblem'
  - oauthprovider.setrequesttokenpath.md: 'OAuthProvider::setRequestTokenPath »'
  - index.md: PHP Manual
  - class.oauthprovider.md: OAuthProvider
title: 'OAuthProvider::setParam'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OAuthProvider::setParam

(PECL OAuth >= 1.0.0)

OAuthProvider::setParam — Встановити параметр

### Опис

```methodsynopsis
final public OAuthProvider::setParam(string $param_key, mixed $param_val = ?): bool
```

Встановлює параметр.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`param_key`

Ключ параметра.

`param_val`

Необов'язкове значення параметра.

Для исключения параметра из процесса проверки подписи установите его в значение\*\*`null`\*\*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [OAuthProvider::addRequiredParameter()](oauthprovider.addrequiredparameter.md) \- Додати необхідні параметри
