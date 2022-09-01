---
navigation:
  - intlchar.chardirection.html: '« IntlChar::charDirection'
  - intlchar.charmirror.html: 'IntlChar::charMirror »'
  - index.html: PHP Manual
  - class.intlchar.html: IntlChar
title: 'IntlChar::charFromName'
---
# IntlChar::charFromName

(PHP 7, PHP 8)

IntlChar::charFromName — Знайти символ Unicode на ім'я та повернути його код

### Опис

```methodsynopsis
public static IntlChar::charFromName(string $name, int $type = IntlChar::UNICODE_CHAR_NAME): ?int
```

Знаходить символ Unicode на ім'я і повертає його код.

Ім'я порівнюється точно та повністю. Якщо ім'я не відповідає символу, то поверне **`false`**

Ім'я Unicode 1.0 вважається таким, що збіглося тільки якщо воно відрізняється від сучасного імені. Усі імена Unicode повинні витись у верхньому регістрі. Розширені імена в нижньому регістрі містять шістнадцяткове значення у фігурних дужках.

### Список параметрів

`name`

Повне ім'я Unicode символ.

`type`

Які типи символів шукати. Одна з констант:

-   **`IntlChar::UNICODE_CHAR_NAME`** (за замовчуванням)
-   **`IntlChar::UNICODE_10_CHAR_NAME`**
-   **`IntlChar::EXTENDED_CHAR_NAME`**
-   **`IntlChar::CHAR_NAME_ALIAS`**
-   **`IntlChar::CHAR_NAME_CHOICE_COUNT`**

### Значення, що повертаються

Значення коду символу Unicode по заданому імені (у вигляді цілого числа (int)), або \*\*`null`\*\*якщо такого символу немає.

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::charFromName("LATIN CAPITAL LETTER A"));
var_dump(IntlChar::charFromName("SNOWMAN"));
var_dump(IntlChar::charFromName("RECYCLING SYMBOL FOR TYPE-1 PLASTICS"));
var_dump(IntlChar::charFromName("A RANDOM STRING WHICH DOESN'T CORRESPOND TO ANY UNICODE CHARACTER"));
?>
```

Результат виконання цього прикладу:

```
int(65)
int(9731)
int(9843)
NULL
```

### Дивіться також

-   [IntlChar::charName()](intlchar.charname.html) - Отримати ім'я Unicode
-   [IntlChar::enumCharNames()](intlchar.enumcharnames.html) - Перераховує всі присвоєні символи Unicode у заданому діапазоні
