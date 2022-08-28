Перетворити рядок з формату "quoted-printable" на 8-бітовий рядок

-   [« imap\_ping](function.imap-ping.html)
    
-   [imap\_rename »](function.imap-rename.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IMAP](ref.imap.html)
    
-   Перетворити рядок з формату "quoted-printable" на 8-бітовий рядок
    

# imapqprint

(PHP 4, PHP 5, PHP 7, PHP 8)

imapqprint — Перетворити рядок з формату "quoted-printable" на 8-бітовий рядок

### Опис

```methodsynopsis
imap_qprint(string $string): string|false
```

Перетворює рядок з формату "quoted-printable" на 8-бітовий рядок відповідно до [» RFC2045](http://www.faqs.org/rfcs/rfc2045)секція 6.7.

### Список параметрів

`string`

Рядок у форматі "quoted-printable"

### Значення, що повертаються

Повертає 8-бітовий рядок або **`false`** у разі виникнення помилки.

### Дивіться також

-   [imap\_8bit()](function.imap-8bit.html) - Конвертує 8-бітний рядок у рядок у форматі quoted-printable