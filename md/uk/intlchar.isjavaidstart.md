---
navigation:
  - intlchar.isjavaidpart.md: '« IntlChar::isJavaIDPart'
  - intlchar.isjavaspacechar.md: 'IntlChar::isJavaSpaceChar »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::isJavaIDStart'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::isJavaIDStart

(PHP 7, PHP 8)

IntlChar::isJavaIDStart — Перевірити, чи символ може бути першим в ідентифікаторі Java

### Опис

```methodsynopsis
public static IntlChar::isJavaIDStart(int|string $codepoint): ?bool
```

Перевіряє, чи може символ бути першим в ідентифікаторі Java.

В дополнение к[IntlChar::isIDStart()](intlchar.isidstart.md) **`true`** повертається для символів із категорій "Sc" (символ грошової одиниці) та "Pc" (з'єднувальна пунктуація).

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (например`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint` може бути першим в ідентифікаторі Java, **`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::isJavaIDStart("A"));
var_dump(IntlChar::isJavaIDStart("$"));
var_dump(IntlChar::isJavaIDStart("\n"));
var_dump(IntlChar::isJavaIDStart("\u{2603}"));
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

-   [IntlChar::isIDStart()](intlchar.isidstart.md) \- Перевірити, чи можна використовувати символ на початку ідентифікатора
-   [IntlChar::isJavaIDPart()](intlchar.isjavaidpart.md) \- Перевірити, чи є символ допустимим в ідентифікаторі Java
-   [IntlChar::isalpha()](intlchar.isalpha.md) \- Перевірити, чи є символ літерою
