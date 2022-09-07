---
navigation:
  - function.join.md: « join
  - function.levenshtein.md: levenshtein »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: lcfirst
---
# lcfirst

(PHP 5> = 5.3.0, PHP 7, PHP 8)

lcfirst — Перетворює перший символ рядка на нижній регістр

### Опис

```methodsynopsis
lcfirst(string $string): string
```

Повертає рядок `string`, перший символ якої було перетворено на нижній регістр, якщо цей символ є буквою.

Приналежність тієї чи іншої символу до буквеним визначається з урахуванням поточної локалі. Це означає, що, наприклад, у локалі "C", що використовується за умовчанням, символ ä не буде перетворений.

### Список параметрів

`string`

Вхідний рядок.

### Значення, що повертаються

Повертає результуючий рядок.

### Приклади

**Приклад #1 Приклад використання **lcfirst()****

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

-   [ucfirst()](function.ucfirst.md) - Перетворює перший символ рядка у верхній регістр
-   [strtolower()](function.strtolower.md) - Перетворює рядок на нижній регістр
-   [strtoupper()](function.strtoupper.md) - Перетворює рядок у верхній регістр
-   [ucwords()](function.ucwords.md) - Перетворює на верхній регістр перший символ кожного слова в рядку
