Завершує сеанс cURL

-   [« Функции cURL](ref.curl.md)
    
-   [curlcopyhandle »](function.curl-copy-handle.html)
    
-   [PHP Manual](index.md)
    
-   [Функции cURL](ref.curl.md)
    
-   Завершує сеанс cURL
    

# curlclose

(PHP 4> = 4.0.2, PHP 5, PHP 7, PHP 8)

curlclose — Завершує сеанс cURL

### Опис

```methodsynopsis
curl_close(CurlHandle $handle): void
```

> **Зауваження**
> 
> Використання функції не має сенсу. До PHP 8.0.0 вона використовувалася для закриття ресурсу.

Завершує сеанс cURL та звільняє всі ресурси. Дескриптор `handle` також знищується.

### Список параметрів

`handle`

Дескриптор cURL, отриманий з [curlinit()](function.curl-init.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Описание                                                                                                |
|--------|---------------------------------------------------------------------------------------------------------|
|        | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.md); раніше, очікувався ресурс (resource). |

### Приклади

**Приклад #1 Ініціалізація сеансу cURL та завантаження веб-сторінки**

```php
<?php
// создание нового ресурса cURL
$ch = curl_init();

// установка URL и других необходимых параметров
curl_setopt($ch, CURLOPT_URL, "http://www.example.com/");
curl_setopt($ch, CURLOPT_HEADER, 0);

// загрузка страницы и выдача её браузеру
curl_exec($ch);

// завершение сеанса и освобождение ресурсов
curl_close($ch);
?>
```

### Дивіться також

-   [curlinit()](function.curl-init.html) - Ініціалізує сеанс cURL
-   [curlmulticlose()](function.curl-multi-close.html) - Закриває набір cURL-дескрипторів