---
navigation:
  - intlchar.getintpropertyminvalue.md: '« IntlChar::getIntPropertyMinValue'
  - intlchar.getnumericvalue.md: 'IntlChar::getNumericValue »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::getIntPropertyValue'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::getIntPropertyValue

(PHP 7, PHP 8)

IntlChar::getIntPropertyValue — Отримати значення властивості Unicode для символу

### Опис

```methodsynopsis
public static IntlChar::getIntPropertyValue(int|string $codepoint, int $property): ?int
```

Отримує значення нумерованої або цілісної властивості Unicode для символу. Також повертаються бінарне та шаблонне значення властивості.

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (наПриклад`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

`property`

Властивість Unicode для відображення (Дивись константи `IntlChar::PROPERTY_*`

### Значення, що повертаються

Повертає чисельне значення для зазначеної властивості, або, для властивостей, що перераховуються, відповідну чисельному значенню константу відповідно до значення перерахованого типу властивості. У разі виникнення помилки повертає **`null`**

Повертає или (для\*\*`false`\*\* **`true`**) для бінарних властивостей Unicode.

Повертає бітовий шаблон шаблонних властивостей.

Повертає якщо `property` не входить у допустимий діапазон або якщо версія Unicode не містить даних для цієї властивості.

### Приклади

**Приклад #1 Тестування різних властивостей**

```php
<?php
var_dump(IntlChar::getIntPropertyValue("A", IntlChar::PROPERTY_ALPHABETIC) === 1);
var_dump(IntlChar::getIntPropertyValue("[", IntlChar::PROPERTY_BIDI_MIRRORED) === 1);
var_dump(IntlChar::getIntPropertyValue("Φ", IntlChar::PROPERTY_BLOCK) === IntlChar::BLOCK_CODE_GREEK);
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(true)
bool(true)
```

### Дивіться також

-   [IntlChar::hasBinaryProperty()](intlchar.hasbinaryproperty.md) \- Перевірити бінарну властивість Unicode для символу
-   [IntlChar::getIntPropertyMinValue()](intlchar.getintpropertyminvalue.md) \- Отримати мінімальне значення для властивості Unicode
-   [IntlChar::getIntPropertyMaxValue()](intlchar.getintpropertymaxvalue.md) \- Отримати мінімальне значення для властивості Unicode
-   [IntlChar::getUnicodeVersion()](intlchar.getunicodeversion.md) \- Отримати версію Unicode
