Повертає рядок із описом останньої помилки поточного сеансу

-   [« curl\_errno](function.curl-errno.html)
    
-   [curl\_escape »](function.curl-escape.html)
    
-   [PHP Manual](index.html)
    
-   [Функции cURL](ref.curl.html)
    
-   Повертає рядок із описом останньої помилки поточного сеансу
    

# curlerror

(PHP 4> = 4.0.3, PHP 5, PHP 7, PHP 8)

curlerror — Повертає рядок із описом останньої помилки поточного сеансу

### Опис

```methodsynopsis
curl_error(CurlHandle $handle): string
```

Повертає зрозуміле повідомлення про помилку для останньої операції cURL.

### Список параметрів

`handle`

Дескриптор cURL, отриманий з [curl\_init()](function.curl-init.html)

### Значення, що повертаються

Повертає повідомлення про помилку або `''` (порожній рядок), якщо помилки не сталося.

### список змін

| Версия | Описание |
| --- | --- |
|  | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.html); раніше, очікувався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **curlerror()****

```php
<?php
// Создаём дескриптор curl к несуществующему адресу
$ch = curl_init('http://404.php.net/');
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);

if(curl_exec($ch) === false)
{
    echo 'Ошибка curl: ' . curl_error($ch);
}
else
{
    echo 'Операция завершена без каких-либо ошибок';
}

// Закрываем дескриптор
curl_close($ch);
?>
```

### Дивіться також

-   [curl\_errno()](function.curl-errno.html) - Повертає код останньої помилки
-   [» Коды ошибок cURL](http://curl.haxx.se/libcurl/c/libcurl-errors.html)