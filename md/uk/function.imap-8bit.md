---
navigation:
  - ref.imap.md: « Функции IMAP
  - function.imap-alerts.html: imapalerts »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imap8bit
---
# imap8bit

(PHP 4, PHP 5, PHP 7, PHP 8)

imap8bit — Конвертує 8-бітний рядок у рядок у форматі quoted-printable

### Опис

```methodsynopsis
imap_8bit(string $string): string|false
```

Конвертує 8-бітний рядок у рядок, закодований механізмом quoted-printable (відповідно до [» RFC2045](http://www.faqs.org/rfcs/rfc2045), Розділ 6.7).

### Список параметрів

`string`

8-бітний рядок для конвертації

### Значення, що повертаються

Повертає рядок формату quoted-printable або **`false`** у разі виникнення помилки.

### Дивіться також

-   [imapqprint()](function.imap-qprint.md) - Перетворити рядок з формату "quoted-printable" на 8-бітовий рядок
