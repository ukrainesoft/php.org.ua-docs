Повертає рядок, що описує помилку

-   [« curlmultisetopt](function.curl-multi-setopt.html)
    
-   [curlpause »](function.curl-pause.html)
    
-   [PHP Manual](index.html)
    
-   [Функции cURL](ref.curl.html)
    
-   Повертає рядок, що описує помилку
    

# curlmultistrerror

(PHP 5> = 5.5.0, PHP 7, PHP 8)

curlmultistrerror — Повертає рядок, що описує помилку

### Опис

```methodsynopsis
curl_multi_strerror(int $error_code): ?string
```

Повертає текст повідомлення про помилку, яка відповідає заданому коду помилки CURLM.

### Список параметрів

`error_code`

Одна та констант [» кодов ошибок CURLM](http://curl.haxx.se/libcurl/c/libcurl-errors.html)

### Значення, що повертаються

Повертає рядок з описом помилки та **`null`**, якщо переданий код неправильний.

### Приклади

**Приклад #1 Приклад використання **curlmultistrerror()****

```php
<?php
// Создаём обработчики curl
$ch1 = curl_init("http://example.com/");
$ch2 = curl_init("http://php.net/");

// Создаём множественный обработчик cURL
$mh = curl_multi_init();

// Добавляем дескрипторы в набор дескрипторов
curl_multi_add_handle($mh, $ch1);
curl_multi_add_handle($mh, $ch2);

// Запускаем множественный обработчик
do {
    $status = curl_multi_exec($mh, $active);
    if ($active) {
        curl_multi_select($mh);
    }
} while ($active && $status === CURLM_OK);

// Проверяем на ошибки
if ($status != CURLM_OK) {
    // Выводим ошибку
    echo "ОШИБКА!\n " . curl_multi_strerror($status);
}
?>
```

### Дивіться також

-   [curlstrerror()](function.curl-strerror.html) - Отримати текстовий опис для коду помилки
-   [» коды ошибок cURL](http://curl.haxx.se/libcurl/c/libcurl-errors.html)