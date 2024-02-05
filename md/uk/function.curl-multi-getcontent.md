---
navigation:
  - function.curl-multi-exec.md: « curl\_multi\_exec
  - function.curl-multi-info-read.md: curl\_multi\_info\_read »
  - index.md: PHP Manual
  - ref.curl.md: Опції cURL
title: curl\_multi\_getcontent
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# curl\_multi\_getcontent

(PHP 5, PHP 7, PHP 8)

curl\_multi\_getcontent — Повернення результату операції, якщо встановлено опцію **`CURLOPT_RETURNTRANSFER`**

### Опис

```methodsynopsis
curl_multi_getcontent(CurlHandle $handle): ?string
```

Якщо для певного дескриптора було встановлено опцію \*\*`CURLOPT_RETURNTRANSFER`\*\*ця функція поверне вміст цього cURL-дескриптора у вигляді рядка.

### Список параметрів

`handle`

Дескриптор cURL, отриманий з [curl\_init()](function.curl-init.md)

### Значення, що повертаються

Повертає вміст cURL-дескриптора, якщо була використана опція \*\*`CURLOPT_RETURNTRANSFER`** або **`null`\*\*якщо опція не була задана.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.md); раніше, очікувався ресурс (resource). |

### Дивіться також

-   [curl\_multi\_init()](function.curl-multi-init.md) \- Створює набір cURL-дескрипторів
