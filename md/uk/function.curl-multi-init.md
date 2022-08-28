Створює набір cURL-дескрипторів

-   [« curl\_multi\_info\_read](function.curl-multi-info-read.html)
    
-   [curl\_multi\_remove\_handle »](function.curl-multi-remove-handle.html)
    
-   [PHP Manual](index.html)
    
-   [Функции cURL](ref.curl.html)
    
-   Створює набір cURL-дескрипторів
    

# curlmultiinit

(PHP 5, PHP 7, PHP 8)

curlmultiinit — Створює набір cURL-дескрипторів

### Опис

```methodsynopsis
curl_multi_init(): CurlMultiHandle
```

Дозволяє асинхронну обробку безлічі cURL-дескрипторів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає набір cURL-дескрипторів у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання повертає екземпляр [CurlMultiHandle](class.curlmultihandle.html); раніше, повертався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **curlmultiinit()****

Цей приклад створить два дескриптори cURL, додасть в набір дескрипторів, а потім запустить їх асинхронно.

```php
<?php
// создаём оба ресурса cURL
$ch1 = curl_init();
$ch2 = curl_init();

// устанавливаем URL и другие соответствующие опции
curl_setopt($ch1, CURLOPT_URL, "http://lxr.php.net/");
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

-   [curl\_init()](function.curl-init.html) - Ініціалізує сеанс cURL
-   [curl\_multi\_close()](function.curl-multi-close.html) - Закриває набір cURL-дескрипторів