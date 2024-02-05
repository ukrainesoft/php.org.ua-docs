---
navigation:
  - function.curl-share-close.md: « curl\_share\_close
  - function.curl-share-init.md: curl\_share\_init »
  - index.md: PHP Manual
  - ref.curl.md: Опції cURL
title: curl\_share\_errno
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# curl\_share\_errno

(PHP 7 >= 7.1.0, PHP 8)

curl\_share\_errno — Повертає код останньої помилки оброблюваного обробника curl

### Опис

```methodsynopsis
curl_share_errno(CurlShareHandle $share_handle): int
```

Повертає код останньої помилки оброблюваного curl, що розділяється, у вигляді цілого числа.

### Список параметрів

`share_handle`

Обробник, що розділяється cURL, повертається [curl\_share\_init()](function.curl-share-init.md)

### Значення, що повертаються

Повертає код останньої помилки оброблюваного curl, що розділяється, у вигляді цілого числа.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція більше не повертає \*\*`false`\*\*в случае возникновения ошибки. |
| 8.0.0 | `share_handle` expects a [CurlShareHandle](class.curlsharehandle.md) instance now; previously, a resource was expected. |

### Дивіться також

-   [curl\_errno()](function.curl-errno.md) \- Повертає код останньої помилки
