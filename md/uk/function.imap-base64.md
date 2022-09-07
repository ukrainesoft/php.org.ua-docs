---
navigation:
  - function.imap-append.md: « imapappend
  - function.imap-binary.md: imapbinary »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapbase64
---
# imapbase64

(PHP 4, PHP 5, PHP 7, PHP 8)

imapbase64 — Декодувати текст закодований BASE64

### Опис

```methodsynopsis
imap_base64(string $string): string|false
```

Декодує текст `string`закодований BASE64.

### Список параметрів

`string`

Закодований текст

### Значення, що повертаються

Повертає рядок з декодованим повідомленням або **`false`** у разі виникнення помилки.

### Дивіться також

-   [imapbinary()](function.imap-binary.md) - Конвертує 8-бітовий рядок у рядок base64
-   [base64encode()](function.base64-encode.md) - Кодує дані у формат MIME base64
-   [base64decode()](function.base64-decode.md) - Декодує дані, закодовані MIME base64
-   [» RFC2045](http://www.faqs.org/rfcs/rfc2045)секція 6.8
