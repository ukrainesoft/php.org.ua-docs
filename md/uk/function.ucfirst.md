---
navigation:
  - function.trim.md: « trim
  - function.ucwords.md: ucwords »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: ucfirst
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ucfirst

(PHP 4, PHP 5, PHP 7, PHP 8)

ucfirst — Перетворює перший символ рядка у верхній регістр

### Опис

```methodsynopsis
ucfirst(string $string): string
```

Повертає рядок `string`, в якій перший символ переведений у верхній регістр, якщо символ є ASCII в діапазоні від `"a"`(0x61) до`"z"`(0x7a).

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

**Приклад #1 Приклад використання функції** ucfirst()\*\*\*\*

```php
<?php
$foo = 'hello world!';
$foo = ucfirst($foo);             // Hello world!

$bar = 'HELLO WORLD!';
$bar = ucfirst($bar);             // HELLO WORLD!
$bar = ucfirst(strtolower($bar)); // Hello world!
?>
```

### Дивіться також

-   [lcfirst()](function.lcfirst.md) \- Перетворює перший символ рядка на нижній регістр
-   [strtolower()](function.strtolower.md) \- Перетворює рядок на нижній регістр
-   [strtoupper()](function.strtoupper.md) \- Перетворює рядок у верхній регістр
-   [ucwords()](function.ucwords.md) \- Перетворює у верхній регістр перший символ кожного слова у рядку
-   [mb\_convert\_case()](function.mb-convert-case.md) \- Змінює регістр символів у рядку
