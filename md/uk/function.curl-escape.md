Кодує рядок як URL

-   [« curl\_error](function.curl-error.html)
    
-   [curl\_exec »](function.curl-exec.html)
    
-   [PHP Manual](index.html)
    
-   [Функции cURL](ref.curl.html)
    
-   Кодує рядок як URL
    

# curlescape

(PHP 5> = 5.5.0, PHP 7, PHP 8)

curlescape — Кодує заданий рядок як URL

### Опис

```methodsynopsis
curl_escape(CurlHandle $handle, string $string): string|false
```

Кодує рядок згідно [» RFC 3986](http://www.faqs.org/rfcs/rfc3986)

### Список параметрів

`handle`

Дескриптор cURL, отриманий з [curl\_init()](function.curl-init.html)

`string`

Рядок для кодування.

### Значення, що повертаються

Повертає екранований рядок або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                  |
|--------|-----------------------------------------------------------------------------------------------------------|
|        | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.html); раніше, очікувався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **curlescape()****

```php
<?php
// Создаём обработчик curl
$ch = curl_init();

// Экранируем строку, которую хотим передать методом GET
$location = curl_escape($ch, 'Hofbräuhaus / München');
// Результат: Hofbr%C3%A4uhaus%20%2F%20M%C3%BCnchen

// Собираем URL по частям
$url = "http://example.com/add_location.php?location={$location}";
// Результат: http://example.com/add_location.php?location=Hofbr%C3%A4uhaus%20%2F%20M%C3%BCnchen

// Посылаем запрос HTTP и закрываем обработчик
curl_setopt($ch, CURLOPT_URL, $url);
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
curl_exec($ch);
curl_close($ch);
?>
```

### Дивіться також

-   [curl\_unescape()](function.curl-unescape.html) - Декодує закодований URL-рядок
-   [urlencode()](function.urlencode.html) - URL-кодування рядка
-   [rawurlencode()](function.rawurlencode.html) - URL-кодування рядка згідно з RFC 3986
-   [» RFC 3986](http://www.faqs.org/rfcs/rfc3986)