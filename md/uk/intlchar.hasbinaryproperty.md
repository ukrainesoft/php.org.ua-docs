---
navigation:
  - intlchar.getunicodeversion.md: '« IntlChar::getUnicodeVersion'
  - intlchar.isalnum.md: 'IntlChar::isalnum »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::hasBinaryProperty'
---
# IntlChar::hasBinaryProperty

(PHP 7, PHP 8)

IntlChar::hasBinaryProperty — Перевірити бінарну властивість Unicode для символу

### Опис

```methodsynopsis
public static IntlChar::hasBinaryProperty(int|string $codepoint, int $property): ?bool
```

Перевіряє бінарну властивість Unicode для символу.

Unicode, особливо у версії 3.2, визначає значно більше властивостей, ніж у оригінальному наборі UnicodeData.txt.

API властивостей служить для відображення властивостей Unicode, як визначено в базі даних символів Unicode (Unicode Character Database або UCD) та технічних звітах Unicode (Unicode Technical Reports або UTR). Більш детальний опис доступний на чайі [» http://www.unicode.org/ucd/](http://www.unicode.org/ucd/). Імена властивостей Unicode дивіться у файлі UCD PropertyAliases.txt.

### Список параметрів

`codepoint`

Цілочисленне (int) завдання коду символу (наприклад `0x2603` для *U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`

`property`

Властивість Unicode для відображення (Дивись константи `IntlChar::PROPERTY_*`

### Значення, що повертаються

Повертає **`true`** або **`false`** залежно від значення бінарної властивості Unicode символу `codepoint`. Також повертає **`false`** якщо `property` знаходиться поза межами або якщо використовується версія Unicode не містить даних для цієї властивості взагалі або конкретно для цього символу. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних властивостей**

```php
<?php
var_dump(IntlChar::hasBinaryProperty("A", IntlChar::PROPERTY_ALPHABETIC));
var_dump(IntlChar::hasBinaryProperty("A", IntlChar::PROPERTY_CASE_SENSITIVE));
var_dump(IntlChar::hasBinaryProperty("A", IntlChar::PROPERTY_BIDI_MIRRORED));
var_dump(IntlChar::hasBinaryProperty("[", IntlChar::PROPERTY_ALPHABETIC));
var_dump(IntlChar::hasBinaryProperty("[", IntlChar::PROPERTY_CASE_SENSITIVE));
var_dump(IntlChar::hasBinaryProperty("[", IntlChar::PROPERTY_BIDI_MIRRORED));
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(true)
bool(false)
bool(false)
bool(false)
bool(true)
```

### Дивіться також

-   [IntlChar::getIntPropertyValue()](intlchar.getintpropertyvalue.md) - Отримати значення властивості Unicode для символу
-   [IntlChar::getUnicodeVersion()](intlchar.getunicodeversion.md) - Отримати версію Unicode
