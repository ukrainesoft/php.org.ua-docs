Конвертує 8-бітний рядок у рядок base64

-   [« imapbase64](function.imap-base64.html)
    
-   [imapbody »](function.imap-body.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Конвертує 8-бітний рядок у рядок base64
    

# imapbinary

(PHP 4, PHP 5, PHP 7, PHP 8)

imapbinary — Конвертує 8-бітний рядок у рядок base64

### Опис

```methodsynopsis
imap_binary(string $string): string|false
```

Конвертує 8-бітний рядок у рядок base64 відповідно до [» RFC2045](http://www.faqs.org/rfcs/rfc2045), секція 6.8.

### Список параметрів

`string`

8-бітний рядок

### Значення, що повертаються

Повертає рядок, кодований у base64 або **`false`** у разі виникнення помилки.

### Дивіться також

-   [imapbase64()](function.imap-base64.html) - Декодувати текст закодований BASE64