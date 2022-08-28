Повертає код останньої помилки

-   [« curl\_copy\_handle](function.curl-copy-handle.html)
    
-   [curl\_error »](function.curl-error.html)
    
-   [PHP Manual](index.html)
    
-   [Функции cURL](ref.curl.html)
    
-   Повертає код останньої помилки
    

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

Дескриптор cURL, отриманий з [curl\_init()](function.curl-init.html)

### Значення, що повертаються

Повертає номер помилки або `0` (нуль), якщо помилки не сталося.

### список змін

| Версия | Описание                                                                                                  |
|--------|-----------------------------------------------------------------------------------------------------------|
|        | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.html); раніше, очікувався ресурс (resource). |

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

-   [curl\_error()](function.curl-error.html) - Повертає рядок із описом останньої помилки поточного сеансу
-   [» Коды ошибок cURL](http://curl.haxx.se/libcurl/c/libcurl-errors.html)