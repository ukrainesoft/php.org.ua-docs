---
navigation:
  - function.curl-multi-close.html: « curlmulticlose
  - function.curl-multi-exec.html: curlmultiexec »
  - index.md: PHP Manual
  - ref.curl.md: Функции cURL
title: curlmultierrno
---
# curlmultierrno

(PHP 7> = 7.1.0, PHP 8)

curlmultierrno — Повертає код останньої помилки множинного curl

### Опис

```methodsynopsis
curl_multi_errno(CurlMultiHandle $multi_handle): int
```

Повертає код останньої помилки множини curl у вигляді цілого числа.

### Список параметрів

`multi_handle`

Мультидескриптор cURL, отриманий з [curlmultiinit()](function.curl-multi-init.html)

### Значення, що повертаються

Повертає код останньої помилки множини curl у вигляді цілого числа.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція більше не повертає **`false`** у разі виникнення помилки. |
|  | `multi_handle` тепер чекає екземпляр; раніше, очікувався ресурс (resource). |

### Дивіться також

-   [curlerrno()](function.curl-errno.html) - Повертає код останньої помилки
