---
navigation:
  - function.imap-base64.md: « imap\_base64
  - function.imap-body.md: imap\_body »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_binary
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_binary

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_binary — Конвертує 8-бітний рядок у рядок base64

### Опис

```methodsynopsis
imap_binary(string $string): string|false
```

Конвертує 8-бітний рядок у рядок base64 відповідно до [» RFC2045](http://www.faqs.org/rfcs/rfc2045), секція 6.8.

### Список параметрів

`string`

8-бітний рядок

### Значення, що повертаються

Повертає рядок, кодований у base64 або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [imap\_base64()](function.imap-base64.md) \- Декодує закодований BASE64 текст
