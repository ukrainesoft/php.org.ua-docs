---
navigation:
  - intlchar.charmirror.md: '« IntlChar::charMirror'
  - intlchar.chartype.md: 'IntlChar::charType »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::charName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::charName

(PHP 7, PHP 8)

IntlChar::charName — Отримати ім'я Unicode

### Опис

```methodsynopsis
public static IntlChar::charName(int|string $codepoint, int $type = IntlChar::UNICODE_CHAR_NAME): ?string
```

Повертає ім'я Unicode.

В зависимости от`type`, повернене ім'я може бути як "сучасним", так і ім'ям, визначеним у Unicode версії 1.0. Ім'я містить лише "незмінювані" символи, такі як A-Z, 0-9, пробіл і '-'. Ім'я Unicode 1.0 повертається тільки якщо воно відрізняється від "сучасного" для даного символу і якщо ICU є запис про нього.

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (наПриклад`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

`type`

Які типи символів шукати. Одна з констант:

-   **`IntlChar::UNICODE_CHAR_NAME`**(default)
-   **`IntlChar::UNICODE_10_CHAR_NAME`**
-   **`IntlChar::EXTENDED_CHAR_NAME`**
-   **`IntlChar::CHAR_NAME_ALIAS`**
-   **`IntlChar::CHAR_NAME_CHOICE_COUNT`**

### Значення, що повертаються

Відповідне ім'я або порожній рядок, якщо символ не має імені, або \*\*`null`\*\*якщо такого символу немає.

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::charName("."));
var_dump(IntlChar::charName(".", IntlChar::UNICODE_CHAR_NAME));
var_dump(IntlChar::charName("\u{2603}"));
var_dump(IntlChar::charName("\u{0000}"));
?>
```

Результат виконання наведеного прикладу:

```
string(9) "FULL STOP"
string(9) "FULL STOP"
string(7) "SNOWMAN"
string(0) ""
```

### Дивіться також

-   [IntlChar::charFromName()](intlchar.charfromname.md) \- Знайти символ Unicode по його імені та повернути його код
-   [IntlChar::enumCharNames()](intlchar.enumcharnames.md) \- Перераховує всі присвоєні символи Unicode у заданому діапазоні
