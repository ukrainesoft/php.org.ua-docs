---
navigation:
  - intlchar.isjavaidpart.html: '« IntlChar::isJavaIDPart'
  - intlchar.isjavaspacechar.html: 'IntlChar::isJavaSpaceChar »'
  - index.html: PHP Manual
  - class.intlchar.html: IntlChar
title: 'IntlChar::isJavaIDStart'
---
# IntlChar::isJavaIDStart

(PHP 7, PHP 8)

IntlChar::isJavaIDStart — Перевірити, чи може символ бути першим в ідентифікаторі Java

### Опис

```methodsynopsis
public static IntlChar::isJavaIDStart(int|string $codepoint): ?bool
```

Перевіряє, чи може символ бути першим в ідентифікаторі Java.

На додаток до [IntlChar::isIDStart()](intlchar.isidstart.html) **`true`** повертається для символів із категорій "Sc" (символ грошової одиниці) та "Pc" (з'єднувальна пунктуація).

### Список параметрів

`codepoint`

Цілочисленне (int) завдання коду символу (наприклад `0x2603` для *U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`

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

Результат виконання цього прикладу:

```
bool(true)
bool(true)
bool(false)
bool(false)
```

### Дивіться також

-   [IntlChar::isIDStart()](intlchar.isidstart.html) - Перевірити, чи можна використовувати символ на початку ідентифікатора
-   [IntlChar::isJavaIDPart()](intlchar.isjavaidpart.html) - Перевірити, чи є символ допустимим в ідентифікаторі Java
-   [IntlChar::isalpha()](intlchar.isalpha.html) - Перевірити, чи є символ літерою
