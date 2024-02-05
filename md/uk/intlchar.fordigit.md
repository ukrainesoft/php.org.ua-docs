---
navigation:
  - intlchar.foldcase.md: '« IntlChar::foldCase'
  - intlchar.getbidipairedbracket.md: 'IntlChar::getBidiPairedBracket »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::forDigit'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::forDigit

(PHP 7, PHP 8)

IntlChar::forDigit — Отримати символ, який представляє задане число в заданій основі

### Опис

```methodsynopsis
public static IntlChar::forDigit(int $digit, int $base = 10): int
```

Визначає уявлення символів для конкретної цифри у зазначеній системі числення.

Якщо значення підстави некоректне, або значення числа не є коректним числом у заданій системі числення, буде повернено `U+0000`

Коректні значення radix лежать у діапазоні від до`36`. Коректні значення digit лежать у діапазоні `0 <= digit < radix`

Якщо digit менше `10`, буде повернуто '0' + digit. В іншому випадку повернеться 'a' + digit – 10.

### Список параметрів

`digit`

Число для перетворення символ.

`base`

Заснування системи числення (за замовчуванням `10`

### Значення, що повертаються

Символьне уявлення (типу string) заданого числа із заданою основою системи числення.

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::forDigit(0));
var_dump(IntlChar::forDigit(3));
var_dump(IntlChar::forDigit(3, 10));
var_dump(IntlChar::forDigit(10));
var_dump(IntlChar::forDigit(10, 16));
?>
```

Результат виконання наведеного прикладу:

```
int(48)
int(51)
int(51)
int(0)
int(97)
```

### Дивіться також

-   [IntlChar::digit()](intlchar.digit.md) \- Отримати десяткове число із символу Unicode із заданою основою
-   [IntlChar::charDigitValue()](intlchar.chardigitvalue.md) \- Отримати десяткову цифру із символу десяткової цифри
-   [IntlChar::isdigit()](intlchar.isdigit.md) \- Перевірити, чи є символ цифрою
-   **`IntlChar::PROPERTY_NUMERIC_TYPE`**
