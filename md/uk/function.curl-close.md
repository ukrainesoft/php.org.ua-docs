---
navigation:
  - ref.curl.md: « Функції cURL
  - function.curl-copy-handle.md: curl\_copy\_handle »
  - index.md: PHP Manual
  - ref.curl.md: Опції cURL
title: curl\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# curl\_close

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

curl\_close — Завершує сеанс cURL

### Опис

```methodsynopsis
curl_close(CurlHandle $handle): void
```

> **Зауваження** :
> 
> Використання функції не має сенсу. До PHP 8.0.0 вона використовувалася для закриття ресурсу.

Завершує сеанс cURL та звільняє всі ресурси. Дескриптор `handle` також знищується.

### Список параметрів

`handle`

Дескриптор cURL, отриманий з [curl\_init()](function.curl-init.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.md); раніше, очікувався ресурс (resource). |

### Приклади

**Приклад #1 Ініціалізація сеансу cURL та завантаження веб-сторінки**

```php
<?php
// создание нового ресурса cURL
$ch = curl_init();

// установка URL и других необходимых параметров
curl_setopt($ch, CURLOPT_URL, "http://www.example.com/");
curl_setopt($ch, CURLOPT_HEADER, 0);

// загрузка страницы и выдача её браузеру
curl_exec($ch);

// завершение сеанса и освобождение ресурсов
curl_close($ch);
?>
```

### Дивіться також

-   [curl\_init()](function.curl-init.md) \- Ініціалізує сеанс cURL
-   [curl\_multi\_close()](function.curl-multi-close.md) \- Закриває набір cURL-дескрипторів
