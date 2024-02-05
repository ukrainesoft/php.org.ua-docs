---
navigation:
  - function.curl-multi-close.md: « curl\_multi\_close
  - function.curl-multi-exec.md: curl\_multi\_exec »
  - index.md: PHP Manual
  - ref.curl.md: Опції cURL
title: curl\_multi\_errno
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# curl\_multi\_errno

(PHP 7 >= 7.1.0, PHP 8)

curl\_multi\_errno — Повертає код останньої помилки множинного curl

### Опис

```methodsynopsis
curl_multi_errno(CurlMultiHandle $multi_handle): int
```

Повертає код останньої помилки множини curl у вигляді цілого числа.

### Список параметрів

`multi_handle`

Мультидескриптор cURL, отриманий з [curl\_multi\_init()](function.curl-multi-init.md)

### Значення, що повертаються

Повертає код останньої помилки множини curl у вигляді цілого числа.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція більше не повертає \*\*`false`\*\*в случае возникновения ошибки. |
| 8.0.0 | `multi_handle` тепер чекає екземпляр; раніше, очікувався ресурс (resource). |

### Дивіться також

-   [curl\_errno()](function.curl-errno.md) \- Повертає код останньої помилки
