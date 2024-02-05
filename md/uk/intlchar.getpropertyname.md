---
navigation:
  - intlchar.getpropertyenum.md: '« IntlChar::getPropertyEnum'
  - intlchar.getpropertyvalueenum.md: 'IntlChar::getPropertyValueEnum »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::getPropertyName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::getPropertyName

(PHP 7, PHP 8)

IntlChar::getPropertyName — Отримати Unicode ім'я властивості

### Опис

```methodsynopsis
public static IntlChar::getPropertyName(int $property, int $type = IntlChar::LONG_PROPERTY_NAME): string|false
```

Повертає ім'я Unicode для заданої якості, як визначено в PropertyAliases.txt.

Крім того, ця функція пов'язує властивість **`IntlChar::PROPERTY_GENERAL_CATEGORY_MASK`** із синтетичним ім'ям "gcm" / "General\_Category\_Mask". Цих імен немає в PropertyAliases.txt.

Ця функція близька до [IntlChar::getPropertyEnum()](intlchar.getpropertyenum.md)

### Список параметрів

`property`

Властивість Unicode для відображення (Дивись константи `IntlChar::PROPERTY_*`

Не можна використовувати **`IntlChar::PROPERTY_INVALID_CODE`**. Також, якщо `property` не входить у допустимий діапазон - повертається **`false`**

`type`

Селектор для вибору імені. Якщо не входить у допустимий діапазон – повертається **`false`**

Усі значення мають довгі імена. Більшість має короткі імена, але не всі. Unicode дозволяє додаткові імена; Якщо існують, вони будуть повернуті з додаванням 1, 2, і т.д **`IntlChar::LONG_PROPERTY_NAME`**

### Значення, що повертаються

Повертає імена або **`false`** якщо `property`или`type` виходять за допустимий діапазон.

Якщо `type` повертає **`false`**, то все більші величини `type` також повернуть **`false`**, з одним винятком: якщо **`false`** повернеться для **`IntlChar::SHORT_PROPERTY_NAME`**, то\*\*`IntlChar::LONG_PROPERTY_NAME`\*\* (і вище) все ще можуть повернути не **`false`**

### Приклади

**Приклад #1 Тестування різних властивостей**

```php
<?php
var_dump(IntlChar::getPropertyName(IntlChar::PROPERTY_BIDI_CLASS));
var_dump(IntlChar::getPropertyName(IntlChar::PROPERTY_BIDI_CLASS, IntlChar::SHORT_PROPERTY_NAME));
var_dump(IntlChar::getPropertyName(IntlChar::PROPERTY_BIDI_CLASS, IntlChar::LONG_PROPERTY_NAME));
var_dump(IntlChar::getPropertyName(IntlChar::PROPERTY_BIDI_CLASS, IntlChar::LONG_PROPERTY_NAME + 1));
?>
```

Результат виконання наведеного прикладу:

```
string(10) "Bidi_Class"
string(2) "bc"
string(10) "Bidi_Class"
bool(false)
```

### Дивіться також

-   [IntlChar::getPropertyEnum()](intlchar.getpropertyenum.md) \- Отримати значення константи властивості на його ім'я
