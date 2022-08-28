Отримати текстовий опис для коду помилки

-   [« curl\_share\_strerror](function.curl-share-strerror.html)
    
-   [curl\_unescape »](function.curl-unescape.html)
    
-   [PHP Manual](index.html)
    
-   [Функции cURL](ref.curl.html)
    
-   Отримати текстовий опис для коду помилки
    

# curlstrerror

(PHP 5> = 5.5.0, PHP 7, PHP 8)

curlstrerror — Отримати текстовий опис для коду помилки

### Опис

```methodsynopsis
curl_strerror(int $error_code): ?string
```

Повертає текстовий опис заданого коду помилки.

### Список параметрів

`error_code`

Одна з констант [» кодов ошибок cURL](http://curl.haxx.se/libcurl/c/libcurl-errors.html)

### Значення, що повертаються

Повертає опис помилки або **`null`**якщо такої помилки немає.

### Приклади

**Приклад #1 Приклад використання [curl\_errno()](function.curl-errno.html)**

```php
<?php
// Создаём обработчик curl с некорректным указанием протокола в URL
$ch = curl_init("htp://example.com/");

// Посылаем запрос
curl_exec($ch);

// Проверяем на ошибки и выводим их описание
if($errno = curl_errno($ch)) {
    $error_message = curl_strerror($errno);
    echo "cURL error ({$errno}):\n {$error_message}";
}

// Закрываем обработчик
curl_close($ch);
?>
```

Результат виконання цього прикладу:

```
cURL error (1):
 Unsupported protocol
```

### Дивіться також

-   [curl\_errno()](function.curl-errno.html) - Повертає код останньої помилки
-   [curl\_error()](function.curl-error.html) - Повертає рядок із описом останньої помилки поточного сеансу
-   [» Коды ошибок Curl](http://curl.haxx.se/libcurl/c/libcurl-errors.html)