---
navigation:
  - function.curl-multi-add-handle.md: « curl\_multi\_add\_handle
  - function.curl-multi-errno.md: curl\_multi\_errno »
  - index.md: PHP Manual
  - ref.curl.md: Опції cURL
title: curl\_multi\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# curl\_multi\_close

(PHP 5, PHP 7, PHP 8)

curl\_multi\_close — Закриває набір cURL-дескрипторів

### Опис

```methodsynopsis
curl_multi_close(CurlMultiHandle $multi_handle): void
```

> **Зауваження** :
> 
> Використання функції не має сенсу. До PHP 8.0.0 вона використовувалася для закриття ресурсу.

Закриває набір cURL дескрипторів.

### Список параметрів

`multi_handle`

Мультидескриптор cURL, отриманий з [curl\_multi\_init()](function.curl-multi-init.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `multi_handle` тепер чекає екземпляр; раніше, очікувався ресурс (resource). |

### Приклади

**Пример #1 Пример использования**curl\_multi\_close()\*\*\*\*

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
curl_close($ch1);
curl_multi_remove_handle($mh, $ch2);
curl_close($ch2);
curl_multi_close($mh);

?>
```

### Дивіться також

-   [curl\_multi\_init()](function.curl-multi-init.md) \- Створює набір cURL-дескрипторів
-   [curl\_close()](function.curl-close.md) \- Завершує сеанс cURL
