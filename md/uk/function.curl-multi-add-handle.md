---
navigation:
  - function.curl-init.md: « curl\_init
  - function.curl-multi-close.md: curl\_multi\_close »
  - index.md: PHP Manual
  - ref.curl.md: Опції cURL
title: curl\_multi\_add\_handle
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# curl\_multi\_add\_handle

(PHP 5, PHP 7, PHP 8)

curl\_multi\_add\_handle — Додає звичайний cURL-дескриптор до набору cURL-дескрипторів

### Опис

```methodsynopsis
curl_multi_add_handle(CurlMultiHandle $multi_handle, CurlHandle $handle): int
```

Додає дескриптор `handle` до набору дескрипторів `multi_handle`

### Список параметрів

`multi_handle`

Мультидескриптор cURL, отриманий з [curl\_multi\_init()](function.curl-multi-init.md)

`handle`

Дескриптор cURL, отриманий з [curl\_init()](function.curl-init.md)

### Значення, що повертаються

Повертає 0 при успіху, або один із кодів помилок **`CURLM_XXX`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `multi_handle` тепер чекає екземпляр; раніше, очікувався ресурс (resource). |
| 8.0.0 | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.md); раніше, очікувався ресурс (resource). |

### Приклади

**Пример #1 Пример использования**curl\_multi\_add\_handle()\*\*\*\*

Цей приклад створить два дескриптори cURL, додасть в набір дескрипторів, а потім запустить їх асинхронно.

```php
<?php
// создаём оба ресурса cURL
$ch1 = curl_init();
$ch2 = curl_init();

// устанавливаем URL и другие соответствующие опции
curl_setopt($ch1, CURLOPT_URL, "http://www.example.com/");
curl_setopt($ch1, CURLOPT_HEADER, 0);
curl_setopt($ch2, CURLOPT_URL, "http://www.php.net/");
curl_setopt($ch2, CURLOPT_HEADER, 0);

//создаём набор дескрипторов cURL
$mh = curl_multi_init();

//добавляем два дескриптора
curl_multi_add_handle($mh,$ch1);
curl_multi_add_handle($mh,$ch2);

//запускаем множественный обработчик
do {
    $status = curl_multi_exec($mh, $active);
    if ($active) {
        curl_multi_select($mh);
    }
} while ($active && $status == CURLM_OK);

//закрываем все дескрипторы
curl_multi_remove_handle($mh, $ch1);
curl_multi_remove_handle($mh, $ch2);
curl_multi_close($mh);
?>
```

### Дивіться також

-   [curl\_multi\_remove\_handle()](function.curl-multi-remove-handle.md) \- Видаляє cURL дескриптор з набору cURL дескрипторів
-   [curl\_multi\_init()](function.curl-multi-init.md) \- Створює набір cURL-дескрипторів
-   [curl\_init()](function.curl-init.md) \- Ініціалізує сеанс cURL
