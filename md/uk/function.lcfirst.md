---
navigation:
  - function.join.md: « join
  - function.levenshtein.md: levenshtein »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: lcfirst
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# lcfirst

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

lcfirst — Перетворює перший символ рядка на нижній регістр

### Опис

```methodsynopsis
lcfirst(string $string): string
```

Повертає рядок `string`, перший символ якої був перетворений на нижній регістр, якщо цей символ є ASCII-символом в діапазоні від `"A"`(0x41) до`"Z"`(0x5a).

### Список параметрів

`string`

Вхідний рядок.

### Значення, що повертаються

Повертає результуючий рядок.

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Перетворення регістру більше не залежить від локалі, встановленої за допомогою функції [setlocale()](function.setlocale.md). . Буде перетворено лише символи ASCII. |

### Приклади

**Приклад #1 Приклад використання** lcfirst()\*\*\*\*

```php
<?php
$foo = 'HelloWorld';
$foo = lcfirst($foo);             // helloWorld

$bar = 'HELLO WORLD!';
$bar = lcfirst($bar);             // hELLO WORLD!
$bar = lcfirst(strtoupper($bar)); // hELLO WORLD!
?>
```

### Дивіться також

-   [ucfirst()](function.ucfirst.md) \- Перетворює перший символ рядка у верхній регістр
-   [strtolower()](function.strtolower.md) \- Перетворює рядок на нижній регістр
-   [strtoupper()](function.strtoupper.md) \- Перетворює рядок у верхній регістр
-   [ucwords()](function.ucwords.md) \- Перетворює у верхній регістр перший символ кожного слова у рядку
