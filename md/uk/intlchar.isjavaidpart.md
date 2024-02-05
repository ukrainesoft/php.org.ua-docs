---
navigation:
  - intlchar.isisocontrol.md: '« IntlChar::isISOControl'
  - intlchar.isjavaidstart.md: 'IntlChar::isJavaIDStart »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::isJavaIDPart'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::isJavaIDPart

(PHP 7, PHP 8)

IntlChar::isJavaIDPart — Перевірити, чи символ допустимий в ідентифікаторі Java

### Опис

```methodsynopsis
public static IntlChar::isJavaIDPart(int|string $codepoint): ?bool
```

Перевіряє, чи символ допустимий в ідентифікаторі Java.

В дополнение к[IntlChar::isIDPart()](intlchar.isidpart.md) **`true`** повертається для категорії "Sc" (символ грошової одиниці).

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (наПриклад`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint` може зустрічатися в ідентифікаторі Java, **`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::isJavaIDPart("A"));
var_dump(IntlChar::isJavaIDPart("$"));
var_dump(IntlChar::isJavaIDPart("\n"));
var_dump(IntlChar::isJavaIDPart("\u{2603}"));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(true)
bool(false)
bool(false)
```

### Дивіться також

-   [IntlChar::isIDIgnorable()](intlchar.isidignorable.md) \- Перевірити, чи символ ігнорується
-   [IntlChar::isIDPart()](intlchar.isidpart.md) \- Перевірити, чи можна використовувати символ в ідентифікаторі
-   [IntlChar::isJavaIDStart()](intlchar.isjavaidstart.md) \- Перевірити, чи може символ бути першим в ідентифікаторі Java
-   [IntlChar::isalpha()](intlchar.isalpha.md) \- Перевірити, чи є символ літерою
-   [IntlChar::isdigit()](intlchar.isdigit.md) \- Перевірити, чи є символ цифрою
