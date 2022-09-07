---
navigation:
  - function.imap-msgno.md: « imapmsgno
  - function.imap-num-msg.md: imapnummsg »
  - index.md: PHP Manual
  - ref.imap.md: Функции IMAP
title: imapmutf7тоutf8
---
# imapmutf7тоutf8

(PHP 5> = 5.3.0, PHP 7, PHP 8)

imapmutf7тоutf8 — Декодувати змінений рядок UTF-7 на UTF-8

### Опис

```methodsynopsis
imap_mutf7_to_utf8(string $string): string|false
```

Декодувати змінений рядок UTF-7 (відповідно до RFC 2060, розділ 5.1.3) у UTF-8.

> **Зауваження**
> 
> Ця функція доступна лише у випадку, якщо libcclient експортує utf8тоmutf7().

### Список параметрів

`string`

Змінений рядок, закодований у UTF-7.

### Значення, що повертаються

Повертає `string`, конвертовану в UTF-8 або **`false`** у разі виникнення помилки.

### Дивіться також

-   [imaputf8тоmutf7()](function.imap-utf8-to-mutf7.md) - Кодувати рядок UTF-8 у змінений UTF-7
