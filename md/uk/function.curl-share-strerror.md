Повертає опис для заданого коду помилки

-   [« curlsharesetopt](function.curl-share-setopt.html)
    
-   [curlstrerror »](function.curl-strerror.html)
    
-   [PHP Manual](index.md)
    
-   [Функции cURL](ref.curl.md)
    
-   Повертає опис для заданого коду помилки
    

# curlsharestrerror

(PHP 7> = 7.1.0, PHP 8)

curlsharestrerror — Повертає опис для заданого коду помилки

### Опис

```methodsynopsis
curl_share_strerror(int $error_code): ?string
```

Повертає опис для заданого коду помилки.

### Список параметрів

`error_code`

Одна з констант: [» Коди помилок cURL](http://curl.haxx.se/libcurl/c/libcurl-errors.html)

### Значення, що повертаються

Повертає опис для заданого коду помилки або \*\*`null`\*\*якщо такого коду не існує.

### Дивіться також

-   [curlshareerrno()](function.curl-share-errno.html) - Повертає код останньої помилки оброблюваного обробника curl
-   [curlstrerror()](function.curl-strerror.html) - Отримати текстовий опис для коду помилки