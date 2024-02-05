---
navigation:
  - intlchar.isxdigit.md: '« IntlChar::isxdigit'
  - intlchar.tolower.md: 'IntlChar::tolower »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::ord'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::ord

(PHP 7, PHP 8)

IntlChar::ord — Отримати код Unicode

### Опис

```methodsynopsis
public static IntlChar::ord(int|string $character): ?int
```

Повертає код Unicode.

Ця функція протилежна дії функції [IntlChar::chr()](intlchar.chr.md)

### Список параметрів

`character`

Целочисленное (int) задание кода символа (например`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Повертає код Unicode у вигляді цілого числа.

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::ord("A"));
var_dump(IntlChar::ord(" "));
var_dump(IntlChar::ord("\u{2603}"));
?>
```

Результат виконання наведеного прикладу:

```
int(65)
int(32)
int(9731)
```

### Дивіться також

-   [IntlChar::chr()](intlchar.chr.md) \- Отримати символ Unicode за його кодом
-   [mb\_ord()](function.mb-ord.md) \- Отримує кодову точку символу Unicode
-   [ord()](function.ord.md) \- Конвертує перший байт рядка до числа від 0 до 255
