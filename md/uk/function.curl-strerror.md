---
navigation:
  - function.curl-share-strerror.md: « curl\_share\_strerror
  - function.curl-unescape.md: curl\_unescape »
  - index.md: PHP Manual
  - ref.curl.md: Опції cURL
title: curl\_strerror
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# curl\_strerror

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

curl\_strerror — Отримати текстовий опис для коду помилки

### Опис

```methodsynopsis
curl_strerror(int $error_code): ?string
```

Повертає текстовий опис заданого коду помилки.

### Список параметрів

`error_code`

Одна из констант[» кодів помилок cURL](http://curl.haxx.se/libcurl/c/libcurl-errors.md)

### Значення, що повертаються

Возвращает описание ошибки или\*\*`null`\*\*якщо такої помилки немає.

### Приклади

**Приклад #1 Приклад использования[curl\_errno()](function.curl-errno.md)**

```php
<?php
// Создаём обработчик curl с некорректным указанием протокола в URL
$ch = curl_init("htp://example.com/");

// Посылаем запрос
curl_exec($ch);

// Проверяем на ошибки и выводим их описание
if($errno = curl_errno($ch)) {
    $error_message = curl_strerror($errno);
    echo "cURL error ({$errno}):\n {$error_message}";
}

// Закрываем обработчик
curl_close($ch);
?>
```

Результат виконання наведеного прикладу:

```
cURL error (1):
 Unsupported protocol
```

### Дивіться також

-   [curl\_errno()](function.curl-errno.md) \- Повертає код останньої помилки
-   [curl\_error()](function.curl-error.md) \- Повертає рядок із описом останньої помилки поточного сеансу
-   [» Коди помилок Curl](http://curl.haxx.se/libcurl/c/libcurl-errors.md)
