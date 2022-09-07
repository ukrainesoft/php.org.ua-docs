---
navigation:
  - intlchar.getnumericvalue.md: '« IntlChar::getNumericValue'
  - intlchar.getpropertyname.md: 'IntlChar::getPropertyName »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::getPropertyEnum'
---
# IntlChar::getPropertyEnum

(PHP 7, PHP 8)

IntlChar::getPropertyEnum — Отримати значення константи властивості на його ім'я

### Опис

```methodsynopsis
public static IntlChar::getPropertyEnum(string $alias): int
```

Повертає значення константи властивості на його ім'я, як задано в PropertyAliases.txt. Приймаються довгі, короткі та інші варіанти імені.

Додатково ця функція пов'язує синтетичне ім'я "gcm" / "GeneralCategoryMask" з властивістю **`IntlChar::PROPERTY_GENERAL_CATEGORY_MASK`**.Цих імен немає в PropertyAliases.txt.

Функція близька до [IntlChar::getPropertyName()](intlchar.getpropertyname.md)

### Список параметрів

`alias`

Ім'я якості. Імена порівнюються за принципом "loose matching", як описано в PropertyValueAliases.txt.

### Значення, що повертаються

Повертає значення константи `IntlChar::PROPERTY_`, або \*\*`IntlChar::PROPERTY_INVALID_CODE`\*\*якщо задане ім'я не відповідає жодній властивості.

### Приклади

**Приклад #1 Тестування різних властивостей**

```php
<?php
var_dump(IntlChar::getPropertyEnum('Bidi_Class') === IntlChar::PROPERTY_BIDI_CLASS);
var_dump(IntlChar::getPropertyEnum('script') === IntlChar::PROPERTY_SCRIPT);
var_dump(IntlChar::getPropertyEnum('IDEOGRAPHIC') === IntlChar::PROPERTY_IDEOGRAPHIC);
var_dump(IntlChar::getPropertyEnum('Some made-up string') === IntlChar::PROPERTY_INVALID_CODE);
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(true)
bool(true)
bool(true)
```

### Дивіться також

-   [IntlChar::getPropertyName()](intlchar.getpropertyname.md) - Отримати Unicode ім'я властивості
