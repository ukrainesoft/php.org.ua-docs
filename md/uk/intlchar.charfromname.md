---
navigation:
  - intlchar.chardirection.md: '« IntlChar::charDirection'
  - intlchar.charmirror.md: 'IntlChar::charMirror »'
  - index.md: PHP Manual
  - class.intlchar.md: IntlChar
title: 'IntlChar::charFromName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

-   **`IntlChar::UNICODE_CHAR_NAME`**(за замовчуванням)
-   **`IntlChar::UNICODE_10_CHAR_NAME`**
-   **`IntlChar::EXTENDED_CHAR_NAME`**
-   **`IntlChar::CHAR_NAME_ALIAS`**
-   **`IntlChar::CHAR_NAME_CHOICE_COUNT`**

### Значення, що повертаються

Значение кода символа Unicode по заданному имени (в виде целого числа (int)), или\*\*`null`\*\*якщо такого символу немає.

### Приклади

**Приклад #1 Тестування різних способів завдання**

```php
<?php
var_dump(IntlChar::charFromName("LATIN CAPITAL LETTER A"));
var_dump(IntlChar::charFromName("SNOWMAN"));
var_dump(IntlChar::charFromName("RECYCLING SYMBOL FOR TYPE-1 PLASTICS"));
var_dump(IntlChar::charFromName("A RANDOM STRING WHICH DOESN'T CORRESPOND TO ANY UNICODE CHARACTER"));
?>
```

Результат виконання наведеного прикладу:

```
int(65)
int(9731)
int(9843)
NULL
```

### Дивіться також

-   [IntlChar::charName()](intlchar.charname.md) \- Отримати ім'я Unicode
-   [IntlChar::enumCharNames()](intlchar.enumcharnames.md) \- Перераховує всі присвоєні символи Unicode у заданому діапазоні
