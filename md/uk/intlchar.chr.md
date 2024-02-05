---
navigation:
  - intlchar.chartype.md: '« IntlChar::charType'
  - intlchar.digit.md: 'IntlChar::digit »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::chr'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::chr

(PHP 7, PHP 8)

IntlChar::chr — Отримати символ Unicode за його кодом

### Опис

```methodsynopsis
public static IntlChar::chr(int|string $codepoint): ?string
```

Повертає рядок, що містить символ Unicode із заданим кодом.

Ця функція протилежна дії функції [IntlChar::ord()](intlchar.ord.md)

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (например`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Повертає рядок, що містить символ Unicode із заданим кодом або \*\*`null`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
$values = ["A", 63, 123, 9731];
foreach ($values as $value) {
    var_dump(IntlChar::chr($value));
}
?>
```

Результат виконання наведеного прикладу:

```
string(1) "A"
string(1) "?"
string(1) "{"
string(3) "☃"
```

### Дивіться також

-   [IntlChar::ord()](intlchar.ord.md) \- Отримати код символ Unicode
-   [mb\_chr()](function.mb-chr.md) \- Повертає символ за значенням кодової точки Unicode
-   [chr()](function.chr.md) \- Генерує односимвольний рядок за заданим числом
