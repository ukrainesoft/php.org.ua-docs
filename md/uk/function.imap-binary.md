---
navigation:
  - function.imap-base64.md: « imapbase64
  - function.imap-body.md: imapbody »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapbinary
---
# imapbinary

(PHP 4, PHP 5, PHP 7, PHP 8)

imapbinary — Конвертує 8-бітний рядок у рядок base64

### Опис

```methodsynopsis
imap_binary(string $string): string|false
```

Конвертує 8-бітний рядок у рядок base64 відповідно до [» RFC2045](http://www.faqs.org/rfcs/rfc2045), секція 6.8.

### Список параметрів

`string`

8-бітний рядок

### Значення, що повертаються

Повертає рядок, кодований у base64 або **`false`** у разі виникнення помилки.

### Дивіться також

-   [imapbase64()](function.imap-base64.md) - Декодувати текст закодований BASE64
