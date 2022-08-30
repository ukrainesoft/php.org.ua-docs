Перетворює рядок, закодований методом quoted-printable у 8-бітовий рядок

-   [« printf](function.printf.md)
    
-   [quotedprintableencode »](function.quoted-printable-encode.html)
    
-   [PHP Manual](index.md)
    
-   [Функції для роботи з рядками](ref.strings.md)
    
-   Перетворює рядок, закодований методом quoted-printable у 8-бітовий рядок
    

# quotedprintabledecode

(PHP 4, PHP 5, PHP 7, PHP 8)

quotedprintabledecode — Перетворює рядок, закодований методом quoted-printable у 8-бітовий рядок

### Опис

```methodsynopsis
quoted_printable_decode(string $string): string
```

Ця функція повертає 8-бітовий бінарний рядок, що відповідає зазначеному рядку в кодуванні quoted-printable (відповідно до розділу 6.7 [» RFC2045](http://www.faqs.org/rfcs/rfc2045), а не розділом 4.5.2 [» RFC2821](http://www.faqs.org/rfcs/rfc2821), тобто додаткові точки не будуть вирізані з початку рядка).

Ця функція подібна до функції [imapqprint()](function.imap-qprint.html), але не вимагає модуля IMAP.

### Список параметрів

`string`

Вхідний рядок.

### Значення, що повертаються

Повертає 8-бітовий бінарний рядок.

### Приклади

**Приклад #1 Приклад використання **quotedprintabledecode()****

```php
<?php

$encoded = quoted_printable_encode('Möchten Sie ein paar Äpfel?');

var_dump($encoded);
var_dump(quoted_printable_decode($encoded));
?>
```

Результат виконання цього прикладу:

```
string(37) "M=C3=B6chten Sie ein paar =C3=84pfel?"
string(29) "Möchten Sie ein paar Äpfel?"
```

### Дивіться також

-   [quotedprintableencode()](function.quoted-printable-encode.html) - Перетворює 8-бітовий рядок за допомогою методу quoted-printable