Декодувати текст закодований BASE64

-   [« imapappend](function.imap-append.html)
    
-   [imapbinary »](function.imap-binary.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Декодувати текст закодований BASE64
    

# imapbase64

(PHP 4, PHP 5, PHP 7, PHP 8)

imapbase64 — Декодувати текст закодований BASE64

### Опис

```methodsynopsis
imap_base64(string $string): string|false
```

Декодує текст `string`закодований BASE64.

### Список параметрів

`string`

Закодований текст

### Значення, що повертаються

Повертає рядок з декодованим повідомленням або **`false`** у разі виникнення помилки.

### Дивіться також

-   [imapbinary()](function.imap-binary.html) - Конвертує 8-бітовий рядок у рядок base64
-   [base64encode()](function.base64-encode.html) - Кодує дані у формат MIME base64
-   [base64decode()](function.base64-decode.html) - Декодує дані, закодовані MIME base64
-   [» RFC2045](http://www.faqs.org/rfcs/rfc2045)секція 6.8