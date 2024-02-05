---
navigation:
  - function.curl-errno.md: « curl\_errno
  - function.curl-escape.md: curl\_escape »
  - index.md: PHP Manual
  - ref.curl.md: Опції cURL
title: curl\_error
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# curl\_error

(PHP 4 >= 4.0.3, PHP 5, PHP 7, PHP 8)

curl\_error — Повертає рядок із описом останньої помилки поточного сеансу

### Опис

```methodsynopsis
curl_error(CurlHandle $handle): string
```

Повертає зрозуміле повідомлення про помилку для останньої операції cURL.

### Список параметрів

`handle`

Дескриптор cURL, отриманий з [curl\_init()](function.curl-init.md)

### Значення, що повертаються

Повертає повідомлення про помилку або `''` (порожній рядок), якщо помилки не сталося.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.md); раніше, очікувався ресурс (resource). |

### Приклади

**Пример #1 Пример использования**curl\_error()\*\*\*\*

```php
<?php
// Создаём дескриптор curl к несуществующему адресу
$ch = curl_init('http://404.php.net/');
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);

if(curl_exec($ch) === false)
{
    echo 'Ошибка curl: ' . curl_error($ch);
}
else
{
    echo 'Операция завершена без каких-либо ошибок';
}

// Закрываем дескриптор
curl_close($ch);
?>
```

### Дивіться також

-   [curl\_errno()](function.curl-errno.md) \- Повертає код останньої помилки
-   [» Коди помилок cURL](http://curl.haxx.se/libcurl/c/libcurl-errors.md)
