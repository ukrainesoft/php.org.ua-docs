---
navigation:
  - function.curl-multi-setopt.md: « curl\_multi\_setopt
  - function.curl-pause.md: curl\_pause »
  - index.md: PHP Manual
  - ref.curl.md: Опції cURL
title: curl\_multi\_strerror
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# curl\_multi\_strerror

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

curl\_multi\_strerror — Повертає рядок, що описує помилку

### Опис

```methodsynopsis
curl_multi_strerror(int $error_code): ?string
```

Повертає текст повідомлення про помилку, яка відповідає заданому коду помилки CURLM.

### Список параметрів

`error_code`

Одна та констант [»Кодів помилок CURLM](http://curl.haxx.se/libcurl/c/libcurl-errors.md)

### Значення, що повертаються

Повертає рядок з описом помилки та **`null`**, якщо переданий код неправильний.

### Приклади

**Приклад #1 Приклад використання** curl\_multi\_strerror()\*\*\*\*

```php
<?php
// Создаём обработчики curl
$ch1 = curl_init("http://example.com/");
$ch2 = curl_init("http://php.net/");

// Создаём множественный обработчик cURL
$mh = curl_multi_init();

// Добавляем дескрипторы в набор дескрипторов
curl_multi_add_handle($mh, $ch1);
curl_multi_add_handle($mh, $ch2);

// Запускаем множественный обработчик
do {
    $status = curl_multi_exec($mh, $active);
    if ($active) {
        curl_multi_select($mh);
    }
} while ($active && $status === CURLM_OK);

// Проверяем на ошибки
if ($status != CURLM_OK) {
    // Выводим ошибку
    echo "ОШИБКА!\n " . curl_multi_strerror($status);
}
?>
```

### Дивіться також

-   [curl\_strerror()](function.curl-strerror.md) \- Отримати текстовий опис для коду помилки
-   [» коди помилок cURL](http://curl.haxx.se/libcurl/c/libcurl-errors.md)
