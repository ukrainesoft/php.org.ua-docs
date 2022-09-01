---
navigation:
  - function.curl-share-setopt.html: « curlsharesetopt
  - function.curl-strerror.html: curlstrerror »
  - index.md: PHP Manual
  - ref.curl.md: Функции cURL
title: curlsharestrerror
---
# curlsharestrerror

(PHP 7> = 7.1.0, PHP 8)

curlsharestrerror — Повертає опис для заданого коду помилки

### Опис

```methodsynopsis
curl_share_strerror(int $error_code): ?string
```

Повертає опис для заданого коду помилки.

### Список параметрів

`error_code`

Одна з констант: [» Коди помилок cURL](http://curl.haxx.se/libcurl/c/libcurl-errors.html)

### Значення, що повертаються

Повертає опис для заданого коду помилки або \*\*`null`\*\*якщо такого коду не існує.

### Дивіться також

-   [curlshareerrno()](function.curl-share-errno.html) - Повертає код останньої помилки оброблюваного обробника curl
-   [curlstrerror()](function.curl-strerror.html) - Отримати текстовий опис для коду помилки
