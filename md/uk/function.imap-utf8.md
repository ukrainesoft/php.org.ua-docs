---
navigation:
  - function.imap-utf8-to-mutf7.md: « imap\_utf8\_to\_mutf7
  - class.imap-connection.md: IMAP\\Connection »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_utf8
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_utf8

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_utf8 — Перетворює MIME-кодований текст на UTF-8

### Опис

```methodsynopsis
imap_utf8(string $mime_encoded_text): string
```

Перетворює задану в параметрі `mime_encoded_text` рядок в UTF-8, якщо заявлене кодування відоме модулю libc-client. В іншому випадку цей текст декодується, але не перетворюється на UTF-8.

### Список параметрів

`mime_encoded_text`

MIME-кодований рядок. Метод кодування MIME та специфікація UTF-8 описані в [» RFC2047](http://www.faqs.org/rfcs/rfc2047) і [» RFC2044](http://www.faqs.org/rfcs/rfc2044)соответственно.

### Значення, що повертаються

Повертає декодований рядок, якщо можливо, перетворений на UTF-8.

### Приклади

**Пример #1 Базовое использование**imap\_utf8()\*\*\*\*

```php
<?php
echo imap_utf8("Johannes =?ISO-8859-1?Q?Schl=FCter?=");
?>
```

Висновок наведеного прикладу буде схожим на:

```
Johannes Schlüter
```

### Дивіться також

-   [imap\_mime\_header\_decode()](function.imap-mime-header-decode.md) \- декодує елементи заголовка
