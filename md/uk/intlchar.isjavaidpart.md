Перевірити, чи є символ допустимим в ідентифікаторі Java

-   [« IntlChar::isISOControl](intlchar.isisocontrol.html)
    
-   [IntlChar::isJavaIDStart »](intlchar.isjavaidstart.html)
    
-   [PHP Manual](index.html)
    
-   [IntlChar](class.intlchar.html)
    
-   Перевірити, чи є символ допустимим в ідентифікаторі Java
    

# IntlChar::isJavaIDPart

(PHP 7, PHP 8)

IntlChar::isJavaIDPart — Перевірити, чи символ допустимий в ідентифікаторі Java

### Опис

```methodsynopsis
public static IntlChar::isJavaIDPart(int|string $codepoint): ?bool
```

Перевіряє, чи символ допустимий в ідентифікаторі Java.

На додаток до [IntlChar::isIDPart()](intlchar.isidpart.html) **`true`** повертається для категорії "Sc" (символ грошової одиниці).

### Список параметрів

`codepoint`

Цілочисленне (int) завдання коду символу (наприклад `0x2603` для *U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`

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

Результат виконання цього прикладу:

```
bool(true)
bool(true)
bool(false)
bool(false)
```

### Дивіться також

-   [IntlChar::isIDIgnorable()](intlchar.isidignorable.html) - Перевірити, чи символ ігнорується
-   [IntlChar::isIDPart()](intlchar.isidpart.html) - Перевірити, чи можна використовувати символ в ідентифікаторі
-   [IntlChar::isJavaIDStart()](intlchar.isjavaidstart.html) - Перевірити, чи може символ бути першим в ідентифікаторі Java
-   [IntlChar::isalpha()](intlchar.isalpha.html) - Перевірити, чи є символ літерою
-   [IntlChar::isdigit()](intlchar.isdigit.html) - Перевірити, чи є символ цифрою