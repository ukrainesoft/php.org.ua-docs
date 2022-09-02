---
navigation:
  - function.imap-ping.md: « imapping
  - function.imap-rename.md: imaprename »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapqprint
---
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

-   [imap8bit()](function.imap-8bit.md) - Конвертує 8-бітний рядок у рядок у форматі quoted-printable
