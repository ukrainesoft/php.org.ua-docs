---
navigation:
  - function.curl-multi-init.md: « curl\_multi\_init
  - function.curl-multi-select.md: curl\_multi\_select »
  - index.md: PHP Manual
  - ref.curl.md: Опції cURL
title: curl\_multi\_remove\_handle
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# curl\_multi\_remove\_handle

(PHP 5, PHP 7, PHP 8)

curl\_multi\_remove\_handle — Видаляє cURL дескриптор із набору cURL дескрипторів.

### Опис

```methodsynopsis
curl_multi_remove_handle(CurlMultiHandle $multi_handle, CurlHandle $handle): int
```

Видаляє вказаний дескриптор `handle` із зазначеного набору дескрипторів `multi_handle`. Після того, як дескриптор `handle` видалено, його можна знову цілком легально використовувати у функції [curl\_exec()](function.curl-exec.md). Вилучення дескриптора `handle` під час використання також зупинить поточну передачу на цьому дескрипторі.

### Список параметрів

`multi_handle`

Мультидескриптор cURL, отриманий з [curl\_multi\_init()](function.curl-multi-init.md)

`handle`

Дескриптор cURL, отриманий з [curl\_init()](function.curl-init.md)

### Значення, що повертаються

У разі успішного виконання повертає 0 або одну з констант \*\*`CURLM_XXX`\*\*де XXX - код помилки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `multi_handle` тепер чекає екземпляр; раніше, очікувався ресурс (resource). |
| 8.0.0 | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.md); раніше, очікувався ресурс (resource). |

### Дивіться також

-   [curl\_init()](function.curl-init.md) \- Ініціалізує сеанс cURL
-   [curl\_multi\_init()](function.curl-multi-init.md) \- Створює набір cURL-дескрипторів
-   [curl\_multi\_add\_handle()](function.curl-multi-add-handle.md) \- Додає звичайний cURL-дескриптор до набору cURL-дескрипторів
