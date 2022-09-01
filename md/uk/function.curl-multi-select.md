---
navigation:
  - function.curl-multi-remove-handle.html: « curlmultiremovehandle
  - function.curl-multi-setopt.html: curlmultisetopt »
  - index.md: PHP Manual
  - ref.curl.md: Функции cURL
title: curlmultiselect
---
# curlmultiselect

(PHP 5, PHP 7, PHP 8)

curlmultiselect — Чекає на активність на будь-якому curlmulti з'єднанні

### Опис

```methodsynopsis
curl_multi_select(CurlMultiHandle $multi_handle, float $timeout = 1.0): int
```

Блокує виконання скрипту, поки якесь із сполук curlmulti не стане активним.

### Список параметрів

`multi_handle`

Мультидескриптор cURL, отриманий з [curlmultiinit()](function.curl-multi-init.html)

`timeout`

Час у секундах для очікування відповіді.

### Значення, що повертаються

У разі успішного виконання повертає кількість дескрипторів, що містяться у наборах дескрипторів. Може повернути 0, якщо не було активності на жодному дескрипторі. У разі невдачі ця функція поверне -1 У випадку виникнення помилки вибірки (з системного виклику вибірки нижче).

### список змін

| Версия | Описание |
| --- | --- |
|  | `multi_handle` тепер чекає екземпляр; раніше, очікувався ресурс (resource). |

### Дивіться також

-   [curlmultiinit()](function.curl-multi-init.html) - Створює набір cURL-дескрипторів
