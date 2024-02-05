---
navigation:
  - function.curl-multi-remove-handle.md: « curl\_multi\_remove\_handle
  - function.curl-multi-setopt.md: curl\_multi\_setopt »
  - index.md: PHP Manual
  - ref.curl.md: Опції cURL
title: curl\_multi\_select
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# curl\_multi\_select

(PHP 5, PHP 7, PHP 8)

curl\_multi\_select — Чекає на активність на будь-якому curl\_multi з'єднанні

### Опис

```methodsynopsis
curl_multi_select(CurlMultiHandle $multi_handle, float $timeout = 1.0): int
```

Блокує виконання скрипту, поки якесь із сполук curl\_multi не стане активним.

### Список параметрів

`multi_handle`

Мультидескриптор cURL, отриманий з [curl\_multi\_init()](function.curl-multi-init.md)

`timeout`

Час у секундах для очікування відповіді.

### Значення, що повертаються

У разі успішного виконання повертає кількість дескрипторів, що містяться у наборах дескрипторів. Може повернути 0, якщо не було активності на жодному дескрипторі. У разі невдачі ця функція поверне -1 У випадку виникнення помилки вибірки (з системного виклику вибірки нижче).

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `multi_handle` тепер чекає екземпляр; раніше, очікувався ресурс (resource). |

### Дивіться також

-   [curl\_multi\_init()](function.curl-multi-init.md) \- Створює набір cURL-дескрипторів
