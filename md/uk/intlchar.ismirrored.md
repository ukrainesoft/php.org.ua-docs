---
navigation:
  - intlchar.islower.md: '« IntlChar::islower'
  - intlchar.isprint.md: 'IntlChar::isprint »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::isMirrored'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::isMirrored

(PHP 7, PHP 8)

IntlChar::isMirrored — Перевірити, якщо символ має властивість Bidi\_Mirrored

### Опис

```methodsynopsis
public static IntlChar::isMirrored(int|string $codepoint): ?bool
```

Перевірити, якщо у символу властивість Bidi\_Mirrored.

Ця властивість зазвичай є у символів, що використовуються в контексті написання справа наліво, які необхідно відобразити "дзеркальними" гліфами.

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (например`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Повертає **`true`**, якщо `codepoint`имеет свойство Bidi\_Mirrored,**`false`** - якщо ні. У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::isMirrored("A"));
var_dump(IntlChar::isMirrored("<"));
var_dump(IntlChar::isMirrored("("));
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(true)
bool(true)
```

### Дивіться також

-   [IntlChar::charMirror()](intlchar.charmirror.md) - Отримати "дзеркальний" символ за кодом
-   **`IntlChar::PROPERTY_BIDI_MIRRORED`**
