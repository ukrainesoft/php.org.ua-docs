---
navigation:
  - intlchar.chr.md: '« IntlChar::chr'
  - intlchar.enumcharnames.md: 'IntlChar::enumCharNames »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::digit'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::digit

(PHP 7, PHP 8)

IntlChar::digit — Отримати десяткове число із символу Unicode із заданою основою

### Опис

```methodsynopsis
public static IntlChar::digit(int|string $codepoint, int $base = 10): int|false|null
```

Повертає десяткове число із символу Unicode із заданою основою.

Если основание не входит в диапазон`2<=radix<=36` або якщо `codepoint` не є коректним символом для цієї основи, повертається **`false`**. Символ є коректною цифрою, якщо виконується хоча б одна з умов:

-   Символ є десяткову цифру. Такі символи входять у глобальну категорію "Nd" (десяткові цифри) та Numeric\_Type є Decimal. І тут повертається відповідна десяткова цифра.
-   Символ є однією з великих латинських букв від 'A' до 'Z'. І тут 'A' - це 10.
-   Символ є однією із малих латинських букв від 'a' до 'z'. І тут 'a' - це 10.
-   Латинські літери з діапазону ASCII (0061..007A, 0041..005A). Також підходять діапазони Повного ASCII (FF41..FF5A, FF21..FF3A).

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (наПриклад`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

`base`

Основание (по умолчанию`10`

### Значення, що повертаються

Повертає десяткове число із символу Unicode із заданою основою або **`false`**, якщо символ некоректний або виходить за рамки основи. У разі виникнення помилки повертає **`null`**

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Логічний тип](language.types.boolean.md)Используйте[оператор ===](language.operators.comparison.md) для перевірки значення, яке повертається цією функцією.

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::digit("0"));
var_dump(IntlChar::digit("3"));
var_dump(IntlChar::digit("A"));
var_dump(IntlChar::digit("A", 16));
?>
```

Результат виконання наведеного прикладу:

```
int(0)
int(3)
bool(false)
int(10)
```

### Дивіться також

-   [IntlChar::forDigit()](intlchar.fordigit.md) \- Отримати символ, що представляє задане число в заданій основі
-   [IntlChar::charDigitValue()](intlchar.chardigitvalue.md) \- Отримати десяткову цифру із символу десяткової цифри
-   [IntlChar::isdigit()](intlchar.isdigit.md) \- Перевірити, чи є символ цифрою
-   **`IntlChar::PROPERTY_NUMERIC_TYPE`**
