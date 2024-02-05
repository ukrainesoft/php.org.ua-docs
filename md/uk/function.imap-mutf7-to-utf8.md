---
navigation:
  - function.imap-msgno.md: « imap\_msgno
  - function.imap-num-msg.md: imap\_num\_msg »
  - index.md: PHP Manual
  - ref.imap.md: Функції IMAP
title: imap\_mutf7\_to\_utf8
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imap\_mutf7\_to\_utf8

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

imap\_mutf7\_to\_utf8 — Декодує змінений рядок UTF-7 на UTF-8

### Опис

```methodsynopsis
imap_mutf7_to_utf8(string $string): string|false
```

Декодувати змінений рядок UTF-7 (відповідно до RFC 2060, розділ 5.1.3) у UTF-8.

> **Зауваження** :
> 
> Ця функція доступна лише у випадку, якщо libcclient експортує utf8\_to\_mutf7().

### Список параметрів

`string`

Змінений рядок, закодований у UTF-7.

### Значення, що повертаються

Повертає `string`, конвертовану в UTF-8 або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [imap\_utf8\_to\_mutf7()](function.imap-utf8-to-mutf7.md) \- Кодує рядок UTF-8 у змінений UTF-7
