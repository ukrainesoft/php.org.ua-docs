---
navigation:
  - function.gmp-legendre.md: « gmp\_legendre
  - function.gmp-mul.md: gmp\_mul »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_mod
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_mod

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_mod — Обчислення залишку від цілого розподілу

### Опис

```methodsynopsis
gmp_mod(GMP|int|string $num1, GMP|int|string $num2): GMP
```

Обчислює залишок від розподілу числа `num1`на`num2`. Результат завжди невід'ємний, знак числа `num2` ігнорується.

### Список параметрів

`num1`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`num2`

Дільник (модуль).

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Об'єкт класу [GMP](class.gmp.md)

### Приклади

**Пример #1 Пример использования**gmp\_mod()\*\*\*\*

```php
<?php
$mod = gmp_mod("8", "3");
echo gmp_strval($mod) . "\n";
?>
```

Результат виконання наведеного прикладу:

```
2
```
