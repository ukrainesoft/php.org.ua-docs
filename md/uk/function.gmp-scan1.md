---
navigation:
  - function.gmp-scan0.md: « gmp\_scan0
  - function.gmp-setbit.md: gmp\_setbit »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_scan1
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_scan1

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_scan1 — Пошук одиниці в числі

### Опис

```methodsynopsis
gmp_scan1(GMP|int|string $num1, int $start): int
```

Сканує `num1`, начиная с бита`start`, Доки не знайде біт встановлений в 1.

### Список параметрів

`num1`

Число, що сканується.

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`start`

Біт початку пошуку.

### Значення, що повертаються

Повертає індекс знайденого біта як числа (int). Якщо таких немає, буде повернуто -1.

### Приклади

**Приклад #1 Приклад використання** gmp\_scan1()\*\*\*\*

```php
<?php
// "1" бит найден в позиции 3. Поиск начинается с 0
$s1 = gmp_init("01000", 2);
echo gmp_scan1($s1, 0) . "\n";

// "1" бит найден в позиции 9. Поиск начинается с 5
$s2 = gmp_init("01000001111", 2);
echo gmp_scan1($s2, 5) . "\n";
?>
```

Результат виконання наведеного прикладу:

```
3
9
```
