---
navigation:
  - function.gmp-rootrem.md: « gmprootrem
  - function.gmp-scan1.md: gmpscan1 »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmpscan0
---
# gmpscan0

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmpscan0 — Пошук нуля в числі

### Опис

```methodsynopsis
gmp_scan0(GMP|int|string $num1, int $start): int
```

Сканує `num1`, починаючи з біта `start`, Доки не знайде біт встановлений в 0.

### Список параметрів

`num1`

Число для сканування.

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`start`

Біт початку сканування.

### Значення, що повертаються

Повертає індекс знайденого біта як числа (int). Індексація починається із нуля.

### Приклади

**Приклад #1 Приклад використання **gmpscan0()****

```php
<?php
// "0" бит найдёт на позиции 3. поиск начинается с 0
$s1 = gmp_init("10111", 2);
echo gmp_scan0($s1, 0) . "\n";

// "0" бит найдёт на позиции 7. поиск начинается с 5
$s2 = gmp_init("101110000", 2);
echo gmp_scan0($s2, 5) . "\n";
?>
```

Результат виконання цього прикладу:

```
3
7
```
