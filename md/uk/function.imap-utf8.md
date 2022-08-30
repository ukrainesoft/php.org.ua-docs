Перетворює MIME-кодований текст на UTF-8

-   [« imaputf8тоmutf7](function.imap-utf8-to-mutf7.html)
    
-   [IMAPConnection »](class.imap-connection.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Перетворює MIME-кодований текст на UTF-8
    

# imaputf8

(PHP 4, PHP 5, PHP 7, PHP 8)

imaputf8 — Перетворює MIME-кодований текст на UTF-8

### Опис

```methodsynopsis
imap_utf8(string $mime_encoded_text): string
```

Перетворює заданий `mime_encoded_text` в UTF-8, якщо заявлене кодування відоме libc-client. В іншому випадку цей текст декодується, але не перетворюється на UTF-8.

### Список параметрів

`mime_encoded_text`

MIME-кодований рядок. Метод кодування MIME та специфікація UTF-8 описані в [» RFC2047](http://www.faqs.org/rfcs/rfc2047) і [» RFC2044](http://www.faqs.org/rfcs/rfc2044) відповідно.

### Значення, що повертаються

Повертає декодований рядок, якщо можливо, перетворений на UTF-8.

### Приклади

**Приклад #1 Базове використання **imaputf8()****

```php
<?php
echo imap_utf8("Johannes =?ISO-8859-1?Q?Schl=FCter?=");
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Johannes Schlüter
```

### Дивіться також

-   [imapmimeheaderdecode()](function.imap-mime-header-decode.html) - Декодувати елементи заголовка