---
navigation:
  - function.imap-utf7-encode.md: « imap\_utf7\_encode
  - function.imap-utf8.md: imap\_utf8 »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_utf8\_to\_mutf7
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_utf8\_to\_mutf7

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

imap\_utf8\_to\_mutf7 — Кодує рядок UTF-8 на змінений UTF-7

### Опис

```methodsynopsis
imap_utf8_to_mutf7(string $string): string|false
```

Кодувати рядок UTF-8 у змінений рядок UTF-7 (відповідно до розділу 5.1.3 стандарту RFC 2060).

> **Зауваження** :
> 
> Ця функція доступна, тільки якщо модуль libcclient експортує utf8\_to\_mutf7().

### Список параметрів

`string`

Закодований у UTF-8 рядок.

### Значення, що повертаються

Повертає `string`, конвертовану в змінену UTF-7 або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [imap\_mutf7\_to\_utf8()](function.imap-mutf7-to-utf8.md) \- Декодує змінений рядок UTF-7 у UTF-8
