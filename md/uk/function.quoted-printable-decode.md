---
navigation:
  - function.printf.md: « printf
  - function.quoted-printable-encode.md: quoted\_printable\_encode »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: quoted\_printable\_decode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# quoted\_printable\_decode

(PHP 4, PHP 5, PHP 7, PHP 8)

quoted\_printable\_decode — Перетворює рядок, закодований методом quoted-printable, на 8-бітний рядок

### Опис

```methodsynopsis
quoted_printable_decode(string $string): string
```

Ця функція повертає 8-бітовий бінарний рядок, що відповідає зазначеному рядку в кодуванні quoted-printable (відповідно до розділу 6.7 [» RFC2045](http://www.faqs.org/rfcs/rfc2045), а не розділом 4.5.2 [» RFC2821](http://www.faqs.org/rfcs/rfc2821), тобто додаткові точки не будуть вирізані з початку рядка).

Ця функція подібна до функції [imap\_qprint()](function.imap-qprint.md), але не вимагає модуля IMAP.

### Список параметрів

`string`

Вхідний рядок.

### Значення, що повертаються

Повертає 8-бітовий бінарний рядок.

### Приклади

**Приклад #1 Приклад використання** quoted\_printable\_decode()\*\*\*\*

```php
<?php

$encoded = quoted_printable_encode('Möchten Sie ein paar Äpfel?');

var_dump($encoded);
var_dump(quoted_printable_decode($encoded));
?>
```

Результат виконання наведеного прикладу:

```
string(37) "M=C3=B6chten Sie ein paar =C3=84pfel?"
string(29) "Möchten Sie ein paar Äpfel?"
```

### Дивіться також

-   [quoted\_printable\_encode()](function.quoted-printable-encode.md) \- Перетворює 8-бітний рядок методом quoted-printable
