---
navigation:
  - function.ctype-cntrl.md: « ctype\_cntrl
  - function.ctype-graph.md: ctype\_graph »
  - index.md: PHP Manual
  - ref.ctype.md: Опції Ctype
title: ctype\_digit
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ctype\_digit

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

ctype\_digit — Перевірка цифрових символів.

### Опис

```methodsynopsis
ctype_digit(mixed $text): bool
```

Перевіряє, чи передано рядок (string) `text` тільки із цифрових символів.

### Список параметрів

`text`

Перевірений рядок.

> **Зауваження** :
> 
> Якщо передано ціле число (int) в діапазоні між -128 і 255 включно, воно буде оброблено як ASCII-код одного символу (до негативних значень буде додано 256, щоб функція могла представити символи з розширеного діапазону ASCII). Інші цілі числа будуть оброблені як рядки, що містять десяткові цифри цілих чисел.

**Увага**

Починаючи з PHP 8.1.0, передача нерядкових аргументів застаріла. У майбутньому аргумент замість ASCII-коду інтерпретуватиметься як рядок. Залежно від передбачуваної поведінки аргумент або перетворюють у рядок (string), або викликають функцію [chr()](function.chr.md)

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо кожен символ рядка `text` — це десяткова цифра, інакше **`false`**. При виклику з порожнім рядком результатом завжди буде **`false`**

### Приклади

**Приклад #1 Приклад використання** ctype\_digit()\*\*\*\*

```php
<?php

$strings = array('1820.20', '10002', 'wsl!12');
foreach ($strings as $testcase) {
    if (ctype_digit($testcase)) {
        echo "Строка $testcase состоит только из цифр.\n";
    } else {
        echo "Строка $testcase не состоит только из цифр.\n";
    }
}
?>
```

Результат виконання наведеного прикладу:

```
Строка 1820.20 не состоит только из цифр.
Строка 10002 состоит только из цифр.
Строка wsl!12 не состоит только из цифр.
```

**Приклад #2 Приклад використання** ctype\_digit()\*\* з порівнянням рядків та цілих чисел\*\*

```php
<?php

$numeric_string = '42';
$integer        = 42;

ctype_digit($numeric_string);  // true
ctype_digit($integer);         // false (ASCII 42 — это символ *)

is_numeric($numeric_string);   // true
is_numeric($integer);          // true
?>
```

### Дивіться також

-   [ctype\_alnum()](function.ctype-alnum.md) \- Перевіряє буквено-цифрові символи
-   [ctype\_xdigit()](function.ctype-xdigit.md) \- Перевіряє шістнадцяткові цифри
-   [is\_numeric()](function.is-numeric.md) \- Перевіряє, чи містить змінне число чи числове рядок
-   [is\_int()](function.is-int.md) \- Перевіряє, чи є змінна ціла кількість
-   [is\_string()](function.is-string.md) \- Перевіряє, чи є тип змінної рядок
-   [IntlChar::isdigit()](intlchar.isdigit.md) \- Перевірити, чи є символ цифрою
