---
navigation:
  - function.trim.html: « trim
  - function.ucwords.html: ucwords »
  - index.html: PHP Manual
  - ref.strings.html: Функції для роботи з рядками
title: ucfirst
---
# ucfirst

(PHP 4, PHP 5, PHP 7, PHP 8)

ucfirst — Перетворює перший символ рядка у верхній регістр

### Опис

```methodsynopsis
ucfirst(string $string): string
```

Повертає рядок `string`, в якій перший символ переведений у верхній регістр, якщо символ є буквою.

Приналежність тієї чи іншої символу до буквеним визначається з урахуванням поточної локалі. Це означає, що, наприклад, у локалі "C", що використовується за умовчанням, символ ä не буде перетворений.

### Список параметрів

`string`

Вхідний рядок.

### Значення, що повертаються

Повертає результуючий рядок.

### Приклади

**Приклад #1 Приклад використання **ucfirst()****

```php
<?php
$foo = 'hello world!';
$foo = ucfirst($foo);             // Hello world!

$bar = 'HELLO WORLD!';
$bar = ucfirst($bar);             // HELLO WORLD!
$bar = ucfirst(strtolower($bar)); // Hello world!
?>
```

### Дивіться також

-   [lcfirst()](function.lcfirst.md) - Перетворює перший символ рядка на нижній регістр
-   [strtolower()](function.strtolower.md) - Перетворює рядок на нижній регістр
-   [strtoupper()](function.strtoupper.md) - Перетворює рядок у верхній регістр
-   [ucwords()](function.ucwords.md) - Перетворює на верхній регістр перший символ кожного слова в рядку
