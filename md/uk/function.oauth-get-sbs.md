---
navigation:
  - ref.oauth.md: « Функции OAuth
  - function.oauth-urlencode.html: oauthurlencode »
  - index.md: PHP Manual
  - ref.oauth.md: Функции OAuth
title: oauthgetsbs
---
# oauthgetsbs

(PECL OAuth >=0.99.7)

oauthgetsbs — Створити базовий рядок підпису (Signature Base String)

### Опис

```methodsynopsis
oauth_get_sbs(string $http_method, string $uri, array $request_parameters = ?): string
```

Створити базовий рядок підпису (Signature Base String) відповідно до pecl/oauth.

### Список параметрів

`http_method`

HTTP метод.

`uri`

URI для кодування.

`request_parameters`

Масив параметрів запиту.

### Значення, що повертаються

Повертає базовий рядок підпису (Signature Base String).
