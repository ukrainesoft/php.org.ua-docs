---
navigation:
  - function.imap-mailboxmsginfo.md: « imap\_mailboxmsginfo
  - function.imap-msgno.md: imap\_msgno »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_mime\_header\_decode
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_mime\_header\_decode

(PHP 4, PHP 5, PHP 7, PHP 8)

imap\_mime\_header\_decode — Декодує елементи заголовка

### Опис

```methodsynopsis
imap_mime_header_decode(string $string): array|false
```

Декодує MIME-розширення заголовка, що не є текстом ASCII (докладніше — [» RFC2047](http://www.faqs.org/rfcs/rfc2047)

### Список параметрів

`string`

MIME-текст

### Значення, що повертаються

Декодовані елементи повертаються в масиві об'єктів, де кожен об'єкт має дві властивості, `charset`и`text`

Якщо елемент не був декодований, або, іншими словами, він є текстом US-ASCII, властивість `charset`будет установлено в значение`default`

Функція повертає \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**imap\_mime\_header\_decode()\*\*\*\*

```php
<?php
$text = "=?ISO-8859-1?Q?Keld_J=F8rn_Simonsen?= <keld@example.com>";

$elements = imap_mime_header_decode($text);
for ($i=0; $i<count($elements); $i++) {
    echo "Charset: {$elements[$i]->charset}\n";
    echo "Text: {$elements[$i]->text}\n\n";
}
?>
```

Результат виконання наведеного прикладу:

```
Charset: ISO-8859-1
Text: Keld Jørn Simonsen

Charset: default
Text:  <keld@example.com>
```

У прикладі вище ми отримаємо два елементи, де перший елемент був раніше закодований в ISO-8859-1, а другий US-ASCII.

### Дивіться також

-   [imap\_utf8()](function.imap-utf8.md) \- Перетворює MIME-кодований текст на UTF-8
