---
navigation:
  - function.quoted-printable-decode.md: « quotedprintabledecode
  - function.quotemeta.md: quotemeta »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: quotedprintableencode
---
# quotedprintableencode

(PHP 5> = 5.3.0, PHP 7, PHP 8)

quotedprintableencode — Перетворює 8-бітовий рядок за допомогою методу quoted-printable

### Опис

```methodsynopsis
quoted_printable_encode(string $string): string
```

Повертає рядок, закодований у формат quoted-printable відповідно до розділу 6.7 [» RFC2045](http://www.faqs.org/rfcs/rfc2045)

Ця функція подібна до функції [imap8bit()](function.imap-8bit.md), крім того, що не вимагає для своєї роботи модуля IMAP.

### Список параметрів

`string`

Вхідний рядок.

### Значення, що повертаються

Повертає закодований рядок.

### Приклади

**Приклад #1 Приклад використання **quotedprintableencode()****

```php
<?php

$encoded = quoted_printable_encode('Möchten Sie ein paar Äpfel?');

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

-   [quotedprintabledecode()](function.quoted-printable-decode.md) - Перетворює рядок, закодований методом quoted-printable у 8-бітовий рядок
-   [iconvmimeencode()](function.iconv-mime-encode.md) - Створює поле MIME-заголовка
