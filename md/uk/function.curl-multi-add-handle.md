Додає звичайний cURL-дескриптор до набору cURL-дескрипторів

-   [« curlinit](function.curl-init.html)
    
-   [curlmulticlose »](function.curl-multi-close.html)
    
-   [PHP Manual](index.html)
    
-   [Функции cURL](ref.curl.html)
    
-   Додає звичайний cURL-дескриптор до набору cURL-дескрипторів
    

# curlmultiaddhandle

(PHP 5, PHP 7, PHP 8)

curlmultiaddhandle — Додає звичайний cURL-дескриптор до набору cURL-дескрипторів

### Опис

```methodsynopsis
curl_multi_add_handle(CurlMultiHandle $multi_handle, CurlHandle $handle): int
```

Додає дескриптор `handle` до набору дескрипторів `multi_handle`

### Список параметрів

`multi_handle`

Мультидескриптор cURL, отриманий з [curlmultiinit()](function.curl-multi-init.html)

`handle`

Дескриптор cURL, отриманий з [curlinit()](function.curl-init.html)

### Значення, що повертаються

Повертає 0 при успіху, або один із кодів помилок **`CURLM_XXX`**

### список змін

| Версия | Описание |
| --- | --- |
|  | `multi_handle` тепер чекає екземпляр; раніше, очікувався ресурс (resource). |
|  | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.html); раніше, очікувався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **curlmultiaddhandle()****

Цей приклад створить два дескриптори cURL, додасть в набір дескрипторів, а потім запустить їх асинхронно.

```php
<?php
// создаём оба ресурса cURL
$ch1 = curl_init();
$ch2 = curl_init();

// устанавливаем URL и другие соответствующие опции
curl_setopt($ch1, CURLOPT_URL, "http://www.example.com/");
curl_setopt($ch1, CURLOPT_HEADER, 0);
curl_setopt($ch2, CURLOPT_URL, "http://www.php.net/");
curl_setopt($ch2, CURLOPT_HEADER, 0);

//создаём набор дескрипторов cURL
$mh = curl_multi_init();

//добавляем два дескриптора
curl_multi_add_handle($mh,$ch1);
curl_multi_add_handle($mh,$ch2);

//запускаем множественный обработчик
do {
    $status = curl_multi_exec($mh, $active);
    if ($active) {
        curl_multi_select($mh);
    }
} while ($active && $status == CURLM_OK);

//закрываем все дескрипторы
curl_multi_remove_handle($mh, $ch1);
curl_multi_remove_handle($mh, $ch2);
curl_multi_close($mh);
?>
```

### Дивіться також

-   [curlmultiremovehandle()](function.curl-multi-remove-handle.html) - Видаляє cURL дескриптор з набору cURL дескрипторів
-   [curlmultiinit()](function.curl-multi-init.html) - Створює набір cURL-дескрипторів
-   [curlinit()](function.curl-init.html) - Ініціалізує сеанс cURL