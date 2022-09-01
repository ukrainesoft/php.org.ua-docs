---
navigation:
  - function.curl-copy-handle.html: « curlcopyhandle
  - function.curl-error.html: curlerror »
  - index.html: PHP Manual
  - ref.curl.html: Функции cURL
title: curlerrno
---
# curlerrno

(PHP 4> = 4.0.3, PHP 5, PHP 7, PHP 8)

curlerrno — Повертає код останньої помилки

### Опис

```methodsynopsis
curl_errno(CurlHandle $handle): int
```

Повертає код помилки останньої операції cURL.

### Список параметрів

`handle`

Дескриптор cURL, отриманий з [curlinit()](function.curl-init.md)

### Значення, що повертаються

Повертає номер помилки або `0` (нуль), якщо помилки не сталося.

### список змін

| Версия | Описание |
| --- | --- |
|  | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.md); раніше, очікувався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **curlerrno()****

```php
<?php
// Создаём дескриптор curl к несуществующему адресу
$ch = curl_init('http://404.php.net/');

// Запускаем
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
curl_exec($ch);

// Проверяем наличие ошибки
if(curl_errno($ch))
{
    echo 'Ошибка curl: ' . curl_error($ch);
}

// Закрываем дескриптор
curl_close($ch);
?>
```

### Дивіться також

-   [curlerror()](function.curl-error.md) - Повертає рядок із описом останньої помилки поточного сеансу
-   [» Коди помилок cURL](http://curl.haxx.se/libcurl/c/libcurl-errors.md)
