---
navigation:
  - function.gmp-rootrem.md: « gmp\_rootrem
  - function.gmp-scan1.md: gmp\_scan1 »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_scan0
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_scan0

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_scan0 — Пошук нуля в числі

### Опис

```methodsynopsis
gmp_scan0(GMP|int|string $num1, int $start): int
```

Сканує `num1`, начиная с бита`start`, Доки не знайде біт встановлений в 0.

### Список параметрів

`num1`

Число для сканування.

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`start`

Біт початку сканування.

### Значення, що повертаються

Повертає індекс знайденого біта як числа (int). Індексація починається із нуля.

### Приклади

**Приклад #1 Приклад використання** gmp\_scan0()\*\*\*\*

```php
<?php
// "0" бит найдёт на позиции 3. поиск начинается с 0
$s1 = gmp_init("10111", 2);
echo gmp_scan0($s1, 0) . "\n";

// "0" бит найдёт на позиции 7. поиск начинается с 5
$s2 = gmp_init("101110000", 2);
echo gmp_scan0($s2, 5) . "\n";
?>
```

Результат виконання наведеного прикладу:

```
3
7
```
