---
navigation:
  - intlchar.chardigitvalue.html: '« IntlChar::charDigitValue'
  - intlchar.charfromname.html: 'IntlChar::charFromName »'
  - index.html: PHP Manual
  - class.intlchar.html: IntlChar
title: 'IntlChar::charDirection'
---
# IntlChar::charDirection

(PHP 7, PHP 8)

IntlChar::charDirection — Отримати категорію напряму листа для символу

### Опис

```methodsynopsis
public static IntlChar::charDirection(int|string $codepoint): ?int
```

Повертає категорію направлення листа для символу, що використовується в [» Двунаправленном алгоритме Unicode (UAX #9)](http://www.unicode.org/reports/tr9/)

> **Зауваження**
> 
> Деякі непризначені символьні коди мають категорії R або AL, тому що вони знаходяться в блоках зарезервованих під написання зліва направо.

### Список параметрів

`codepoint`

Цілочисленне (int) завдання коду символу (наприклад `0x2603` для *U+2603 СНІГОВИКА*), або символ закодований рядок UTF-8 (наприклад `"\u{2603}"`

### Значення, що повертаються

Значення категорії направлення листа, одна з констант:

-   **`IntlChar::CHAR_DIRECTION_LEFT_TO_RIGHT`**
-   **`IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT`**
-   **`IntlChar::CHAR_DIRECTION_EUROPEAN_NUMBER`**
-   **`IntlChar::CHAR_DIRECTION_EUROPEAN_NUMBER_SEPARATOR`**
-   **`IntlChar::CHAR_DIRECTION_EUROPEAN_NUMBER_TERMINATOR`**
-   **`IntlChar::CHAR_DIRECTION_ARABIC_NUMBER`**
-   **`IntlChar::CHAR_DIRECTION_COMMON_NUMBER_SEPARATOR`**
-   **`IntlChar::CHAR_DIRECTION_BLOCK_SEPARATOR`**
-   **`IntlChar::CHAR_DIRECTION_SEGMENT_SEPARATOR`**
-   **`IntlChar::CHAR_DIRECTION_WHITE_SPACE_NEUTRAL`**
-   **`IntlChar::CHAR_DIRECTION_OTHER_NEUTRAL`**
-   **`IntlChar::CHAR_DIRECTION_LEFT_TO_RIGHT_EMBEDDING`**
-   **`IntlChar::CHAR_DIRECTION_LEFT_TO_RIGHT_OVERRIDE`**
-   **`IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT_ARABIC`**
-   **`IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT_EMBEDDING`**
-   **`IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT_OVERRIDE`**
-   **`IntlChar::CHAR_DIRECTION_POP_DIRECTIONAL_FORMAT`**
-   **`IntlChar::CHAR_DIRECTION_DIR_NON_SPACING_MARK`**
-   **`IntlChar::CHAR_DIRECTION_BOUNDARY_NEUTRAL`**
-   **`IntlChar::CHAR_DIRECTION_FIRST_STRONG_ISOLATE`**
-   **`IntlChar::CHAR_DIRECTION_LEFT_TO_RIGHT_ISOLATE`**
-   **`IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT_ISOLATE`**
-   **`IntlChar::CHAR_DIRECTION_POP_DIRECTIONAL_ISOLATE`**
-   **`IntlChar::CHAR_DIRECTION_CHAR_DIRECTION_COUNT`**

У разі виникнення помилки повертає **`null`**

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::charDirection("A") === IntlChar::CHAR_DIRECTION_LEFT_TO_RIGHT);
var_dump(IntlChar::charDirection("\u{05E9}") === IntlChar::CHAR_DIRECTION_RIGHT_TO_LEFT);
var_dump(IntlChar::charDirection("+") === IntlChar::CHAR_DIRECTION_EUROPEAN_NUMBER_SEPARATOR);
var_dump(IntlChar::charDirection(".") === IntlChar::CHAR_DIRECTION_COMMON_NUMBER_SEPARATOR);
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(true)
bool(true)
bool(true)
```
