---
navigation:
  - function.curl-share-setopt.md: « curl\_share\_setopt
  - function.curl-strerror.md: curl\_strerror »
  - index.md: PHP Manual
  - ref.curl.md: Опції cURL
title: curl\_share\_strerror
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# curl\_share\_strerror

(PHP 7 >= 7.1.0, PHP 8)

curl\_share\_strerror — Повертає опис для заданого коду помилки

### Опис

```methodsynopsis
curl_share_strerror(int $error_code): ?string
```

Повертає опис для заданого коду помилки.

### Список параметрів

`error_code`

Одна из констант:[» Коди помилок cURL](http://curl.haxx.se/libcurl/c/libcurl-errors.md)

### Значення, що повертаються

Возвращает описание для заданного кода ошибки или\*\*`null`\*\*якщо такого коду не існує.

### Дивіться також

-   [curl\_share\_errno()](function.curl-share-errno.md) \- Повертає код останньої помилки оброблюваного обробника curl
-   [curl\_strerror()](function.curl-strerror.md) \- Отримати текстовий опис для коду помилки
