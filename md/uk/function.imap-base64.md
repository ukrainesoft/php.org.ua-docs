---
navigation:
  - function.imap-append.md: « imap\_append
  - function.imap-binary.md: imap\_binary »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_base64
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_base64

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_base64 - Декодує закодований BASE64 текст

### Опис

```methodsynopsis
imap_base64(string $string): string|false
```

Декодує текст `string`закодований BASE64.

### Список параметрів

`string`

Закодований текст

### Значення, що повертаються

Повертає рядок з декодованим повідомленням або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [imap\_binary()](function.imap-binary.md) \- Конвертує 8-бітовий рядок у рядок base64
-   [base64\_encode()](function.base64-encode.md) \- Кодує дані у формат MIME base64
-   [base64\_decode()](function.base64-decode.md) \- Декодує дані, закодовані MIME base64
-   [» RFC2045](http://www.faqs.org/rfcs/rfc2045)секція 6.8
