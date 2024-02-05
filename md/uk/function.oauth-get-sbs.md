---
navigation:
  - ref.oauth.md: « Функції OAuth
  - function.oauth-urlencode.md: oauth\_urlencode »
  - index.md: PHP Manual
  - ref.oauth.md: Функції OAuth
title: oauth\_get\_sbs
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oauth\_get\_sbs

(PECL OAuth >=0.99.7)

oauth\_get\_sbs — Створити базовий рядок підпису (Signature Base String)

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
