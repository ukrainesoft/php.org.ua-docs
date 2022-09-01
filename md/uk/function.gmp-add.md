---
navigation:
  - function.gmp-abs.html: « gmpabs
  - function.gmp-and.html: gmpand »
  - index.html: PHP Manual
  - ref.gmp.html: GMP Функції
title: gmpadd
---
# gmpadd

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmpadd — Складання чисел

### Опис

```methodsynopsis
gmp_add(GMP|int|string $num1, GMP|int|string $num2): GMP
```

Складає два числа.

### Список параметрів

`num1`

Перший доданок.

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`num2`

Другий доданок.

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Сума аргументів як GMP числа.

### Приклади

**Приклад #1 Приклад використання **gmpadd()****

```php
<?php
$sum = gmp_add("123456789012345", "76543210987655");
echo gmp_strval($sum) . "\n";
?>
```

Результат виконання цього прикладу:

```
200000000000000
```
