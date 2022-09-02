---
navigation:
  - function.imap-mailboxmsginfo.md: « imapmailboxmsginfo
  - function.imap-msgno.md: imapmsgno »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapmimeheaderdecode
---
# imapmimeheaderdecode

(PHP 4, PHP 5, PHP 7, PHP 8)

imapmimeheaderdecode — Декодувати елементи заголовка

### Опис

```methodsynopsis
imap_mime_header_decode(string $string): array|false
```

Декодує MIME-розширення заголовка, що не є текстом ASCII (див. [» RFC2047](http://www.faqs.org/rfcs/rfc2047)

### Список параметрів

`string`

MIME-текст

### Значення, що повертаються

Декодовані елементи повертаються в масиві об'єктів, де кожен об'єкт має дві властивості, `charset` і `text`

Якщо елемент не був декодований, або, іншими словами, він є текстом US-ASCII, властивість `charset` буде встановлено на значення `default`

Функція повертає **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **imapmimeheaderdecode()****

```php
<?php
$text = "=?ISO-8859-1?Q?Keld_J=F8rn_Simonsen?= <keld@example.com>";

$elements = imap_mime_header_decode($text);
for ($i=0; $i<count($elements); $i++) {
    echo "Charset: {$elements[$i]->charset}\n";
    echo "Text: {$elements[$i]->text}\n\n";
}
?>
```

Результат виконання цього прикладу:

```
Charset: ISO-8859-1
Text: Keld Jørn Simonsen

Charset: default
Text:  <keld@example.com>
```

У прикладі вище ми отримаємо два елементи, де перший елемент був раніше закодований в ISO-8859-1, а другий US-ASCII.

### Дивіться також

-   [imaputf8()](function.imap-utf8.md) - Перетворює MIME-кодований текст на UTF-8
