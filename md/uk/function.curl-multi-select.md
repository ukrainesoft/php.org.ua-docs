Чекає активності на будь-якому curlmulti з'єднанні

-   [« curl\_multi\_remove\_handle](function.curl-multi-remove-handle.html)
    
-   [curl\_multi\_setopt »](function.curl-multi-setopt.html)
    
-   [PHP Manual](index.html)
    
-   [Функции cURL](ref.curl.html)
    
-   Чекає активності на будь-якому curlmulti з'єднанні
    

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

Мультидескриптор cURL, отриманий з [curl\_multi\_init()](function.curl-multi-init.html)

`timeout`

Час у секундах для очікування відповіді.

### Значення, що повертаються

У разі успішного виконання повертає кількість дескрипторів, що містяться у наборах дескрипторів. Може повернути 0, якщо не було активності на жодному дескрипторі. У разі невдачі ця функція поверне -1 У випадку виникнення помилки вибірки (з системного виклику вибірки нижче).

### список змін

| Версия | Описание |
| --- | --- |
|  | `multi_handle` тепер чекає екземпляр; раніше, очікувався ресурс (resource). |

### Дивіться також

-   [curl\_multi\_init()](function.curl-multi-init.html) - Створює набір cURL-дескрипторів