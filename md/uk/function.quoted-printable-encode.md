Перетворює 8-бітовий рядок за допомогою методу quoted-printable

-   [« quoted\_printable\_decode](function.quoted-printable-decode.html)
    
-   [quotemeta »](function.quotemeta.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы со строками](ref.strings.html)
    
-   Перетворює 8-бітовий рядок за допомогою методу quoted-printable
    

# quotedprintableencode

(PHP 5> = 5.3.0, PHP 7, PHP 8)

quotedprintableencode — Перетворює 8-бітовий рядок за допомогою методу quoted-printable

### Опис

```methodsynopsis
quoted_printable_encode(string $string): string
```

Повертає рядок, закодований у формат quoted-printable відповідно до розділу 6.7 [» RFC2045](http://www.faqs.org/rfcs/rfc2045)

Ця функція подібна до функції [imap\_8bit()](function.imap-8bit.html), крім того, що не вимагає для своєї роботи модуля IMAP.

### Список параметрів

`string`

Вхідний рядок.

### Значення, що повертаються

Повертає закодований рядок.

### Приклади

**Приклад #1 Приклад використання **quotedprintableencode()****

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

-   [quoted\_printable\_decode()](function.quoted-printable-decode.html) - Перетворює рядок, закодований методом quoted-printable у 8-бітовий рядок
-   [iconv\_mime\_encode()](function.iconv-mime-encode.html) - Створює поле MIME-заголовка