---
navigation:
  - function.curl-multi-info-read.md: « curl\_multi\_info\_read
  - function.curl-multi-remove-handle.md: curl\_multi\_remove\_handle »
  - index.md: PHP Manual
  - ref.curl.md: Опції cURL
title: curl\_multi\_init
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# curl\_multi\_init

(PHP 5, PHP 7, PHP 8)

curl\_multi\_init — Створює набір cURL-дескрипторів

### Опис

```methodsynopsis
curl_multi_init(): CurlMultiHandle
```

Дозволяє асинхронну обробку безлічі cURL-дескрипторів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає набір cURL-дескрипторів.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання повертає екземпляр [CurlMultiHandle](class.curlmultihandle.md); раніше, повертався ресурс (resource). |

### Приклади

**Пример #1 Пример использования**curl\_multi\_init()\*\*\*\*

Цей приклад створить два дескриптори cURL, додасть в набір дескрипторів, а потім запустить їх асинхронно.

```php
<?php
// создаём оба ресурса cURL
$ch1 = curl_init();
$ch2 = curl_init();

// устанавливаем URL и другие соответствующие опции
curl_setopt($ch1, CURLOPT_URL, "http://lxr.php.net/");
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

-   [curl\_init()](function.curl-init.md) \- Ініціалізує сеанс cURL
-   [curl\_multi\_close()](function.curl-multi-close.md) \- Закриває набір cURL-дескрипторів
