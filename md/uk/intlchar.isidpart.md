---
navigation:
  - intlchar.isidignorable.md: '« IntlChar::isIDIgnorable'
  - intlchar.isidstart.md: 'IntlChar::isIDStart »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::isIDPart'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::isIDPart

(PHP 7, PHP 8)

IntlChar::isIDPart — Перевірити, чи можна використовувати символ в ідентифікаторі

### Опис

```methodsynopsis
public static IntlChar::isIDPart(int|string $codepoint): ?bool
```

Перевіряє, чи можна використовувати символ в ідентифікаторі.

**`true`** для символів категорії "L" (літери), "Nl" (символи цифр), "Nd" (десяткові цифри), "Mc" та "Mn" (мітки суміщення), "Pc" (з'єднувальна пунктуація), та u\_isIDIgnorable(c).

> **Зауваження** :
> 
> Майже те саме, що і ID\_Continue в Unicode (**`IntlChar::PROPERTY_ID_CONTINUE`**) за винятком того, що Unicode рекомендує ігнорувати Cf, які менше [IntlChar::isIDIgnorable()](intlchar.isidignorable.md)

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (наПриклад`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Повертає **`true`** якщо `codepoint` можна використовувати в ідентифікаторах, **`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::isIDPart("A"));
var_dump(IntlChar::isIDPart("$"));
var_dump(IntlChar::isIDPart("\n"));
var_dump(IntlChar::isIDPart("\u{2603}"));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(false)
bool(false)
bool(false)
```

### Дивіться також

-   [IntlChar::isIDIgnorable()](intlchar.isidignorable.md) \- Перевірити, чи символ ігнорується
-   [IntlChar::isIDStart()](intlchar.isidstart.md) \- Перевірити, чи можна використовувати символ на початку ідентифікатора
-   **`IntlChar::PROPERTY_ID_CONTINUE`**
