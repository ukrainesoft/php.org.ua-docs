---
navigation:
  - function.curl-multi-add-handle.md: « curlmultiaddhandle
  - function.curl-multi-errno.md: curlmultierrno »
  - index.md: PHP Manual
  - ref.curl.md: Функции cURL
title: curlmulticlose
---
# curlmulticlose

(PHP 5, PHP 7, PHP 8)

curlmulticlose — Закриває набір cURL-дескрипторів

### Опис

```methodsynopsis
curl_multi_close(CurlMultiHandle $multi_handle): void
```

> **Зауваження**
> 
> Використання функції не має сенсу. До PHP 8.0.0 вона використовувалася для закриття ресурсу.

Закриває набір cURL дескрипторів.

### Список параметрів

`multi_handle`

Мультидескриптор cURL, отриманий з [curlmultiinit()](function.curl-multi-init.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Описание |
| --- | --- |
|  | `multi_handle` тепер чекає екземпляр; раніше, очікувався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **curlmulticlose()****

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
curl_close($ch1);
curl_multi_remove_handle($mh, $ch2);
curl_close($ch2);
curl_multi_close($mh);

?>
```

### Дивіться також

-   [curlmultiinit()](function.curl-multi-init.md) - Створює набір cURL-дескрипторів
-   [curlclose()](function.curl-close.md) - Завершує сеанс cURL
