---
navigation:
  - oauthprovider.calltokenhandler.md: '« OAuthProvider::calltokenHandler'
  - oauthprovider.construct.md: 'OAuthProvider::\_\_construct »'
  - index.md: PHP Manual
  - class.oauthprovider.md: OAuthProvider
title: 'OAuthProvider::checkOAuthRequest'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OAuthProvider::checkOAuthRequest

(PECL OAuth >= 1.0.0)

OAuthProvider::checkOAuthRequest — Перевірка запиту oauth

### Опис

```methodsynopsis
public OAuthProvider::checkOAuthRequest(string $uri = ?, string $method = ?): void
```

Перевіряє запит OAuth.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`uri`

Необов'язковий URI або кінцева точка.

`method`

Необов'язковий параметр, який визначає метод HTTP. Одна з **`OAUTH_HTTP_METHOD_*`** [констант OAuth](oauth.constants.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викликає помилку рівня \*\*`E_ERROR`\*\*если HTTP-метод задан некорректно.

### Дивіться також

-   [OAuthProvider::reportProblem()](oauthprovider.reportproblem.md) \- Повідомити про проблему
