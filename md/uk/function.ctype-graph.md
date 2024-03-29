---
navigation:
  - function.ctype-digit.md: « ctype\_digit
  - function.ctype-lower.md: ctype\_lower »
  - index.md: PHP Manual
  - ref.ctype.md: Опції Ctype
title: ctype\_graph
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ctype\_graph

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

ctype\_graph — Перевіряє будь-які друковані символи, крім пробілу

### Опис

```methodsynopsis
ctype_graph(mixed $text): bool
```

Перевіряє, чи передано рядок (string) `text` тільки з видимих ​​під час друку символів.

### Список параметрів

`text`

Перевірений рядок.

> **Зауваження** :
> 
> Якщо передано ціле число (int) в діапазоні між -128 і 255 включно, воно буде оброблено як ASCII-код одного символу (до негативних значень буде додано 256, щоб функція могла представити символи з розширеного діапазону ASCII). Інші цілі числа будуть оброблені як рядки, що містять десяткові цифри цілих чисел.

**Увага**

Починаючи з PHP 8.1.0, передача нерядкових аргументів застаріла. У майбутньому аргумент замість ASCII-коду інтерпретуватиметься як рядок. Залежно від передбачуваної поведінки аргумент або перетворюють у рядок (string), або викликають функцію [chr()](function.chr.md)

### Значення, що повертаються

Повертає **`true`**, якщо кожен символ у рядку `text` друкований і фактично створює видимий висновок (без пропуску), інакше **`false`**. При виклику з порожнім рядком результатом завжди буде **`false`**

### Приклади

**Приклад #1 Приклад використання функції** ctype\_graph()\*\*\*\*

```php
<?php

$strings = array('string1' => "asdf\n\r\t", 'string2' => 'arf12', 'string3' => 'LKA#@%.54');
foreach ($strings as $name => $testcase) {
    if (ctype_graph($testcase)) {
        echo "Строка '$name' состоит только из (видимых) печатных символов.\n";
    } else {
        echo "Строка '$name' не состоит только из (видимых) печатных символов.\n";
    }
}
?>
```

Результат виконання наведеного прикладу:

```
Строка 'string1' не состоит только из (видимых) печатных символов.
Строка 'string2' состоит только из (видимых) печатных символов.
Строка 'string3' состоит только из (видимых) печатных символов.
```

### Дивіться також

-   [ctype\_alnum()](function.ctype-alnum.md) \- Перевіряє буквено-цифрові символи
-   [ctype\_print()](function.ctype-print.md) \- Перевіряє друковані символи
-   [ctype\_punct()](function.ctype-punct.md) \- Перевіряє друковані символи, які не містять пробілових або буквено-цифрових символів
-   [IntlChar::isgraph()](intlchar.isgraph.md) \- Перевірити, чи є символом графічним символом
