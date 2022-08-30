Перевірити, якщо у символу властивість BidiMirrored

-   [« IntlChar::islower](intlchar.islower.md)
    
-   [IntlChar::isprint »](intlchar.isprint.md)
    
-   [PHP Manual](index.md)
    
-   [IntlChar](class.intlchar.md)
    
-   Перевірити, якщо у символу властивість BidiMirrored
    

# IntlChar::isMirrored

(PHP 7, PHP 8)

IntlChar::isMirrored — Перевірити, якщо символ має властивість BidiMirrored

### Опис

```methodsynopsis
public static IntlChar::isMirrored(int|string $codepoint): ?bool
```

Перевірити, якщо у символу властивість BidiMirrored.

Ця властивість зазвичай є у символів, що використовуються в контексті написання справа наліво, які необхідно відобразити "дзеркальними" гліфами.

### Список параметрів

`codepoint`

Цілочисленне (int) завдання коду символу (наприклад `0x2603` для *U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint` має властивість BidiMirrored, **`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::isMirrored("A"));
var_dump(IntlChar::isMirrored("<"));
var_dump(IntlChar::isMirrored("("));
?>
```

Результат виконання цього прикладу:

```
bool(false)
bool(true)
bool(true)
```

### Дивіться також

-   [IntlChar::charMirror()](intlchar.charmirror.md) - Отримати "дзеркальний" символ за кодом
-   **`IntlChar::PROPERTY_BIDI_MIRRORED`**