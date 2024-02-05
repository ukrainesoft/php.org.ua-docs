---
navigation:
  - function.gmp-fact.md: « gmp\_fact
  - function.gmp-gcdext.md: gmp\_gcdext »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_gcd
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_gcd

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_gcd - Обчислення найбільшого спільного дільника

### Опис

```methodsynopsis
gmp_gcd(GMP|int|string $num1, GMP|int|string $num2): GMP
```

Обчислює найбільший спільний дільник чисел `num1`и`num2`. Результат завжди позитивний, навіть якщо одне з чисел, або обидва негативні.

### Список параметрів

`num1`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`num2`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Позитивний НОД чисел `num1`и`num2`

### Приклади

**Пример #1 Пример использования**gmp\_gcd()\*\*\*\*

```php
<?php
$gcd = gmp_gcd("12", "21");
echo gmp_strval($gcd) . "\n";
?>
```

Результат виконання наведеного прикладу:

```
3
```

### Дивіться також

-   [gmp\_lcm()](function.gmp-lcm.md) \- обчислює найменше загальне кратне
