---
navigation:
  - function.curl-copy-handle.md: « curl\_copy\_handle
  - function.curl-error.md: curl\_error »
  - index.md: PHP Manual
  - ref.curl.md: Опції cURL
title: curl\_errno
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# curl\_errno

(PHP 4 >= 4.0.3, PHP 5, PHP 7, PHP 8)

curl\_errno — Повертає код останньої помилки

### Опис

```methodsynopsis
curl_errno(CurlHandle $handle): int
```

Повертає код помилки останньої операції cURL.

### Список параметрів

`handle`

Дескриптор cURL, отриманий з [curl\_init()](function.curl-init.md)

### Значення, що повертаються

Повертає номер помилки або (нуль), якщо помилки не сталося.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.md); раніше, очікувався ресурс (resource). |

### Приклади

**Пример #1 Пример использования**curl\_errno()\*\*\*\*

```php
<?php
// Создаём дескриптор curl к несуществующему адресу
$ch = curl_init('http://404.php.net/');

// Запускаем
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
curl_exec($ch);

// Проверяем наличие ошибки
if(curl_errno($ch))
{
    echo 'Ошибка curl: ' . curl_error($ch);
}

// Закрываем дескриптор
curl_close($ch);
?>
```

### Дивіться також

-   [curl\_error()](function.curl-error.md) \- Повертає рядок із описом останньої помилки поточного сеансу
-   [» Коди помилок cURL](http://curl.haxx.se/libcurl/c/libcurl-errors.md)
