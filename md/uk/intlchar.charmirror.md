---
navigation:
  - intlchar.charfromname.md: '« IntlChar::charFromName'
  - intlchar.charname.md: 'IntlChar::charName »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::charMirror'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# IntlChar::charMirror

(PHP 7, PHP 8)

IntlChar::charMirror — Отримати "дзеркальний" символ за кодом

### Опис

```methodsynopsis
public static IntlChar::charMirror(int|string $codepoint): int|string|null
```

Зв'язує вказаний символ із дзеркальним відображенням.

Для символів із властивістю *Bidi\_Mirrored*, іноді необхідно отримати зв'язок з іншим символом Unicode, який можна використовувати як дзеркальне відображення гліфа заданого символу. Такий спосіб перетворення тексту і з кодувань з візуального порядку "для бідних". Також корисно для дисплеїв без вибору гліфа.

### Список параметрів

`codepoint`

Целочисленное (int) задание кода символа (например`0x2603`для*U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`) .

### Значення, що повертаються

Повертає інший код символу Unicode, який можна використовувати як дзеркальне відображення заданого або `codepoint`, якщо відповідного символу не знайшлося або якщо `codepoint`не имеет свойства*Bidi\_Mirrored*

Тип, що повертається повинен бути int, якщо тільки символ не був переданий як рядок UTF-8 (string), у цьому випадку повернеться рядок (string). У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::charMirror("A"));
var_dump(IntlChar::charMirror("<"));
var_dump(IntlChar::charMirror("("));
?>
```

Результат виконання наведеного прикладу:

```
string(1) "A"
string(1) ">"
string(2) ")"
```

### Дивіться також

-   [IntlChar::isMirrored()](intlchar.ismirrored.md) \- Перевірити, якщо у символу властивість Bidi\_Mirrored
-   **`IntlChar::PROPERTY_BIDI_MIRRORED`**
