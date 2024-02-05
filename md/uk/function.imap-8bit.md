---
navigation:
  - ref.imap.md: « Функції IMAP
  - function.imap-alerts.md: imap\_alerts »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_8bit
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_8bit

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_8bit — Конвертує 8-бітний рядок у рядок у форматі quoted-printable

### Опис

```methodsynopsis
imap_8bit(string $string): string|false
```

Конвертує 8-бітний рядок у рядок, закодований механізмом quoted-printable (відповідно до [» RFC2045](http://www.faqs.org/rfcs/rfc2045), Розділ 6.7).

### Список параметрів

`string`

8-бітний рядок для конвертації

### Значення, що повертаються

Повертає рядок формату quoted-printable або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [imap\_qprint()](function.imap-qprint.md) \- Перетворює рядок з формату quoted-printable на 8-бітовий рядок
