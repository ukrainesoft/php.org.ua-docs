---
navigation:
  - function.str-getcsv.md: « str\_getcsv
  - function.str-ireplace.md: str\_ireplace »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: str\_increment
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# str\_increment

(PHP 8 >= 8.3.0)

str\_increment — Збільшує на одиницю літерно-цифровий рядок

### Опис

```methodsynopsis
str_increment(string $string): string
```

Повертає збільшений літерно-цифровий рядок `string`, що складається з символів кодування ASCII.

### Список параметрів

`string`

Вхідний рядок.

### Значення, що повертаються

Повертає збільшений літерно-цифровий рядок, що складається з ASCII- символів.

### Помилки

Буде викинуто виняток [ValueError](class.valueerror.md), якщо вхідний рядок `string`пустая.

Буде викинуто виняток [ValueError](class.valueerror.md), якщо вхідний рядок `string` складається не з ASCII- символів.

### Приклади

**Приклад #1 Базовий приклад використання **str\_increment()****

```php
<?php
$str = 'ABC';
var_dump(str_increment($str));
?>
```

Результат виконання наведеного прикладу:

```
string(3) "ABD"
```

**Приклад #2 Приклад використання** str\_increment()\*\* з перенесенням (збільшенням вищого розряду чи розрядності)\*\*

```php
<?php
$str = 'DZ';
var_dump(str_increment($str));

$str = 'ZZ';
var_dump(str_increment($str));
?>
```

Результат виконання наведеного прикладу:

```
string(2) "EA"
string(3) "AAA"
```

### Дивіться також

-   [str\_decrement()](function.str-decrement.md) \- Зменшує на одиницю буквено-цифровий рядок
