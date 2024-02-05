---
navigation:
  - function.gmp-cmp.md: « gmp\_cmp
  - function.gmp-div-q.md: gmp\_div\_q »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_com
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_com

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_com — Обчислює доповнення до одиниці числа

### Опис

```methodsynopsis
gmp_com(GMP|int|string $num): GMP
```

Повертає доповнення до одиниці числа `num`

### Список параметрів

`num`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Повертає доповнення до одиниці числа `num` як числа GMP.

### Приклади

**Пример #1 Пример использования**gmp\_com()\*\*\*\*

```php
<?php
$com = gmp_com("1234");
echo gmp_strval($com) . "\n";
?>
```

Результат виконання наведеного прикладу:

```
-1235
```
