Перевірити, чи в нижньому регістрі символ

-   [« IntlChar::isJavaSpaceChar](intlchar.isjavaspacechar.html)
    
-   [IntlChar::isMirrored »](intlchar.ismirrored.html)
    
-   [PHP Manual](index.html)
    
-   [IntlChar](class.intlchar.html)
    
-   Перевірити, чи в нижньому регістрі символ
    

# IntlChar::islower

(PHP 7, PHP 8)

IntlChar::islower — Перевірити, чи в нижньому регістрі символ

### Опис

```methodsynopsis
public static IntlChar::islower(int|string $codepoint): ?bool
```

Визначає, чи символ входить до категорії "Ll" (літери в нижньому регістрі).

> **Зауваження**
> 
> Деякі символи можуть бути пропущені, оскільки вони можуть мати іншу головну категорію. Щоб не втратити їх - використовуйте функцію [IntlChar::isULowercase()](intlchar.isulowercase.html)

### Список параметрів

`codepoint`

Цілочисленне (int) завдання коду символу (наприклад `0x2603` для *U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint` входить до категорії Ll або **`false`**, якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::islower("A"));
var_dump(IntlChar::islower("a"));
var_dump(IntlChar::islower("Φ"));
var_dump(IntlChar::islower("φ"));
var_dump(IntlChar::islower("1"));
?>
```

Результат виконання цього прикладу:

```
bool(false)
bool(true)
bool(false)
bool(true)
bool(false)
```

### Дивіться також

-   [IntlChar::isupper()](intlchar.isupper.html) - Перевірити, чи входить символ у категорію "Lu" (літера у верхньому регістрі)
-   [IntlChar::istitle()](intlchar.istitle.html) - Перевірити, чи символ є титульним (Titlecase)
-   [IntlChar::tolower()](intlchar.tolower.html) - Перетворення символу Unicode на нижній регістр
-   [IntlChar::toupper()](intlchar.toupper.html) - Перетворення символу Unicode у верхній регістр
-   **`IntlChar::PROPERTY_LOWERCASE`**