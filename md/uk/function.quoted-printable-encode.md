---
navigation:
  - function.quoted-printable-decode.md: « quoted\_printable\_decode
  - function.quotemeta.md: quotemeta »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: quoted\_printable\_encode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# quoted\_printable\_encode

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

quoted\_printable\_encode — Перетворює 8-бітовий рядок методом quoted-printable

### Опис

```methodsynopsis
quoted_printable_encode(string $string): string
```

Повертає рядок, закодований у формат quoted-printable відповідно до розділу 6.7 [» RFC2045](http://www.faqs.org/rfcs/rfc2045)

Ця функція подібна до функції [imap\_8bit()](function.imap-8bit.md), крім того, що не вимагає для своєї роботи модуля IMAP.

### Список параметрів

`string`

Вхідний рядок.

### Значення, що повертаються

Повертає закодований рядок.

### Приклади

**Пример #1 Пример использования**quoted\_printable\_encode()\*\*\*\*

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

-   [quoted\_printable\_decode()](function.quoted-printable-decode.md) \- Перетворює рядок, закодований методом quoted-printable, на 8-бітовий рядок
-   [iconv\_mime\_encode()](function.iconv-mime-encode.md) \- Створює поле MIME-заголовка
