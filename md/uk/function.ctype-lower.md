---
navigation:
  - function.ctype-graph.md: « ctype\_graph
  - function.ctype-print.md: ctype\_print »
  - index.md: PHP Manual
  - ref.ctype.md: Опції Ctype
title: ctype\_lower
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ctype\_lower

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

ctype\_lower — Перевірка символів у нижньому регістрі

### Опис

```methodsynopsis
ctype_lower(mixed $text): bool
```

Перевіряє, чи передано рядок (string) `text` лише з літер у нижньому регістрі.

### Список параметрів

`text`

Перевірений рядок.

> **Зауваження** :
> 
> Якщо передано ціле число (int) в діапазоні між -128 і 255 включно, воно буде оброблено як ASCII-код одного символу (до негативних значень буде додано 256, щоб функція могла представити символи з розширеного діапазону ASCII). Інші цілі числа будуть оброблені як рядки, що містять десяткові цифри цілих чисел.

**Увага**

Починаючи з PHP 8.1.0, передача нерядкових аргументів застаріла. У майбутньому аргумент замість ASCII-коду інтерпретуватиметься як рядок. Залежно від передбачуваної поведінки аргумент або перетворюють у рядок (string), або викликають функцію [chr()](function.chr.md)

### Значення, що повертаються

Повертає **`true`**, якщо кожен символ у рядку `text` - Це мала літера поточного мовного стандарту (локалі). При виклику з порожнім рядком результатом завжди буде **`false`**

### Приклади

**Приклад #1 Приклад використання функції** ctype\_lower()**(с использованием локали по умолчанию)**

```php
<?php

$strings = array('aac123', 'qiutoas', 'QASsdks');
foreach ($strings as $testcase) {
    if (ctype_lower($testcase)) {
        echo "Строка $testcase состоит только из букв в нижнем регистре.\n";
    } else {
        echo "Строка $testcase не состоит только из букв в нижнем регистре.\n";
    }
}
?>
```

Результат виконання наведеного прикладу:

```
Строка aac123 не состоит только из букв в нижнем регистре.
Строка qiutoas состоит только из букв в нижнем регистре.
Строка QASsdks не состоит только из букв в нижнем регистре.
```

### Дивіться також

-   [ctype\_alpha()](function.ctype-alpha.md) \- Перевіряє буквені символи
-   [ctype\_upper()](function.ctype-upper.md) \- Перевіряє символи у верхньому регістрі
-   [setlocale()](function.setlocale.md) \- Встановлює налаштування локалі
-   [IntlChar::islower()](intlchar.islower.md) \- Перевірити, чи в нижньому регістрі символ
