---
navigation:
  - function.ctype-alpha.md: « ctype\_alpha
  - function.ctype-digit.md: ctype\_digit »
  - index.md: PHP Manual
  - ref.ctype.md: Опції Ctype
title: ctype\_cntrl
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ctype\_cntrl

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

ctype\_cntrl — Перевіряє символи керування

### Опис

```methodsynopsis
ctype_cntrl(mixed $text): bool
```

Перевіряє, чи передано рядок (string) `text` лише з керуючих символів. До керуючих символів, наприклад, відносяться переклад рядка, символ табуляції, escape.

### Список параметрів

`text`

Перевірений рядок.

> **Зауваження** :
> 
> Якщо передано ціле число (int) в діапазоні між -128 і 255 включно, воно буде оброблено як ASCII-код одного символу (до негативних значень буде додано 256, щоб функція могла представити символи з розширеного діапазону ASCII). Інші цілі числа будуть оброблені як рядки, що містять десяткові цифри цілих чисел.

**Увага**

Починаючи з PHP 8.1.0, передача нерядкових аргументів застаріла. У майбутньому аргумент замість ASCII-коду інтерпретуватиметься як рядок. Залежно від передбачуваної поведінки аргумент або перетворюють у рядок (string), або викликають функцію [chr()](function.chr.md)

### Значення, що повертаються

Повертає **`true`**, якщо кожен символ у рядку `text` належить керуючим символам поточного мовного стандарту (локалі), інакше **`false`**. При виклику з порожнім рядком результатом завжди буде **`false`**

### Приклади

**Приклад #1 Приклад використання функції** ctype\_cntrl()\*\*\*\*

```php
<?php

$strings = array('string1' => "\n\r\t", 'string2' => 'arf12');
foreach ($strings as $name => $testcase) {
    if (ctype_cntrl($testcase)) {
        echo "Строка '$name' состоит только из управляющих символов.\n";
    } else {
        echo "Строка '$name' не состоит только из управляющих символов.\n";
    }
}
?>
```

Результат виконання наведеного прикладу:

```
Строка 'string1' состоит только из управляющих символов.
Строка 'string2' не состоит только из управляющих символов.
```

### Дивіться також

-   [ctype\_print()](function.ctype-print.md) \- Перевіряє друковані символи
-   [IntlChar::iscntrl()](intlchar.iscntrl.md) \- Перевірити, чи є символ керуючим
