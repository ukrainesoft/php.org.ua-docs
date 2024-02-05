---
navigation:
  - function.str-contains.md: « str\_contains
  - function.str-ends-with.md: str\_ends\_with »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: str\_decrement
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# str\_decrement

(PHP 8 >= 8.3.0)

str\_decrement — Зменшує на одиницю літерно-цифровий рядок

### Опис

```methodsynopsis
str_decrement(string $string): string
```

Повертає зменшений літерно-цифровий рядок `string`, що складається з символів кодування ASCII.

### Список параметрів

`string`

Вхідний рядок.

### Значення, що повертаються

Повертає зменшений літерно-цифровий рядок, що складається з ASCII- символів.

### Помилки

Буде викинуто виняток [ValueError](class.valueerror.md), якщо вхідний рядок `string`пустая.

Буде викинуто виняток [ValueError](class.valueerror.md), якщо вхідний рядок `string` складається не з ASCII- символів.

Буде викинуто виняток [ValueError](class.valueerror.md), якщо вхідний рядок `string` не може бути зменшено. Наприклад, `"A"`или`"0"`

### Приклади

**Приклад #1 Базовий приклад використання **str\_decrement()****

```php
<?php
$str = 'ABC';
var_dump(str_decrement($str));
?>
```

Результат виконання наведеного прикладу:

```
string(3) "ABB"
```

**Пример #2 Пример использования**str\_decrement()\*\* з перенесенням (зменшенням вищого розряду чи розрядності)\*\*

```php
<?php
$str = 'ZA';
var_dump(str_decrement($str));

$str = 'AA';
var_dump(str_decrement($str));
?>
```

Результат виконання наведеного прикладу:

```
string(2) "YZ"
string(1) "Z"
```

### Дивіться також

-   [str\_increment()](function.str-increment.md) \- Збільшує на одиницю буквено-цифровий рядок
