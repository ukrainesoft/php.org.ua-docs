---
navigation:
  - intlchar.digit.md: '« IntlChar::digit'
  - intlchar.enumchartypes.md: 'IntlChar::enumCharTypes »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::enumCharNames'
---
# IntlChar::enumCharNames

(PHP 7, PHP 8)

IntlChar::enumCharNames — Перераховує всі символи Unicode, що були присвоєні в заданому діапазоні

### Опис

```methodsynopsis
public static IntlChar::enumCharNames(    int|string $start,    int|string $end,    callable $callback,    int $type = IntlChar::UNICODE_CHAR_NAME): ?bool
```

Перелічує всі присвоєні символи Unicode в заданому діапазоні (включаючи початок діапазону та виключаючи кінець) і для кожного з них функцію, передаючи код символу та його ім'я.

Для імен Unicode 1.0 перераховуються ті символи, імена яких відмінні від своїх " сучасних " імен.

### Список параметрів

`start`

Код символу, з якого починається діапазон.

`end`

Код символу, з якого починається діапазон. Сам цей символ у діапазон не потрапить.

`callback`

Функція, яка буде викликана для кожного символу. До неї будуть передані такі три аргументи:

-   int `$codepoint` - код символу
-   int `$nameChoice` - значення з `type`, дивіться опис нижче
-   string `$name` - Ім'я символу

`type`

Категорія символів для переліку. Одна з констант:

-   **`IntlChar::UNICODE_CHAR_NAME`** (за замовчуванням)
-   **`IntlChar::UNICODE_10_CHAR_NAME`**
-   **`IntlChar::EXTENDED_CHAR_NAME`**
-   **`IntlChar::CHAR_NAME_ALIAS`**
-   **`IntlChar::CHAR_NAME_CHOICE_COUNT`**

### Значення, що повертаються

Повертає **`null`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Перелік діапазону символів**

```php
<?php
IntlChar::enumCharNames(0x2600, 0x2610, function($codepoint, $nameChoice, $name) {
    printf("U+%04x %s\n", $codepoint, $name);
});
?>
```

Результат виконання цього прикладу:

```
U+2600 BLACK SUN WITH RAYS
U+2601 CLOUD
U+2602 UMBRELLA
U+2603 SNOWMAN
U+2604 COMET
U+2605 BLACK STAR
U+2606 WHITE STAR
U+2607 LIGHTNING
U+2608 THUNDERSTORM
U+2609 SUN
U+260a ASCENDING NODE
U+260b DESCENDING NODE
U+260c CONJUNCTION
U+260d OPPOSITION
U+260e BLACK TELEPHONE
U+260f WHITE TELEPHONE
```

### Дивіться також

-   [IntlChar::charName()](intlchar.charname.md) - Отримати ім'я Unicode
-   [IntlChar::charFromName()](intlchar.charfromname.md) - Знайти символ Unicode на ім'я і повернути його код
