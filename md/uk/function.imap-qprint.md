---
navigation:
  - function.imap-ping.md: « imap\_ping
  - function.imap-rename.md: imap\_rename »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_qprint
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_qprint

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_qprint — Перетворює рядок з формату quoted-printable на 8-бітовий рядок

### Опис

```methodsynopsis
imap_qprint(string $string): string|false
```

Перетворює рядок з формату quoted-printable на 8-бітовий рядок так, як це зазначено в розділі 6.7 стандарту [» RFC2045](http://www.faqs.org/rfcs/rfc2045)

### Список параметрів

`string`

Рядок у форматі "quoted-printable"

### Значення, що повертаються

Повертає 8-бітовий рядок або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [imap\_8bit()](function.imap-8bit.md) \- Конвертує 8-бітний рядок у рядок у форматі quoted-printable
