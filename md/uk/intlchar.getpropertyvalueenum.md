---
navigation:
  - intlchar.getpropertyname.md: '« IntlChar::getPropertyName'
  - intlchar.getpropertyvaluename.md: 'IntlChar::getPropertyValueName »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::getPropertyValueEnum'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::getPropertyValueEnum

(PHP 7, PHP 8)

IntlChar::getPropertyValueEnum — Повернути числовий ідентифікатор властивості на ім'я

### Опис

```methodsynopsis
public static IntlChar::getPropertyValueEnum(int $property, string $name): int
```

Повертає числовий ідентифікатор властивості Unicode на його ім'я, як визначено у файлі PropertyValueAliases.txt. Приймаються довгі, короткі та інші варіанти імені.

> **Зауваження** :
> 
> Деякі імена PropertyValueAliases.txt можуть бути вилучені тільки за допомогою **`IntlChar::PROPERTY_GENERAL_CATEGORY_MASK`**, а не\*\*`IntlChar::PROPERTY_GENERAL_CATEGORY`\*\*. Включно з:
> 
> -   "C" / "Інше"
> -   "L" / "Літери"
> -   "LC" / "Літери, що мають кілька регістрів"
> -   "M" / "Мітки"
> -   "N" / "Числа"
> -   "P" / "Пунктуація"
> -   "S" / "Символи"
> -   "Z" / "Розділювачі"

### Список параметрів

`property`

Властивість Unicode для відображення (Дивись константи `IntlChar::PROPERTY_*`

Якщо не входить у допустимий діапазон, або якщо метод не працює з цим значенням, повертається **`IntlChar::PROPERTY_INVALID_CODE`**

`name`

Ім'я якості. Імена порівнюються за принципом "loose matching", як описано в PropertyValueAliases.txt.

### Значення, що повертаються

Повертає відповідне ціле чисельне значення або **`IntlChar::PROPERTY_INVALID_CODE`** якщо відповідність не знайдена або якщо властивість є некоректною.

### Приклади

**Приклад #1 Тестування різних властивостей**

```php
<?php
var_dump(IntlChar::getPropertyValueEnum(IntlChar::PROPERTY_BLOCK, 'greek') === IntlChar::BLOCK_CODE_GREEK);
var_dump(IntlChar::getPropertyValueEnum(IntlChar::PROPERTY_BIDI_CLASS, 'RIGHT_TO_LEFT') === IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT);
var_dump(IntlChar::getPropertyValueEnum(IntlChar::PROPERTY_BIDI_CLASS, 'some made-up string') === IntlChar::PROPERTY_INVALID_CODE);
var_dump(IntlChar::getPropertyValueEnum(123456789, 'RIGHT_TO_LEFT') === IntlChar::PROPERTY_INVALID_CODE);
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(true)
bool(true)
bool(true)
```
