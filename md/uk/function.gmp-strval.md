---
navigation:
  - function.gmp-sqrtrem.md: « gmp\_sqrtrem
  - function.gmp-sub.md: gmp\_sub »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_strval
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_strval

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_strval — Перетворює числа GMP на рядок

### Опис

```methodsynopsis
gmp_strval(GMP|int|string $num, int $base = 10): string
```

Перетворює GMP-число на рядок у системі числення параметра `base`. За замовчуванням числа перетворюються на десяткову систему числення.

### Список параметрів

`num`

GMP число для конвертації.

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`base`

Система числення числа, що повертається. За замовчуванням - 10. Можливі значення: від 2 до 62 та від -2 до -36.

### Значення, що повертаються

Число у вигляді рядка (string).

### Приклади

**Приклад #1 Перетворення GMP-числа на рядок**

```php
<?php
$a = gmp_init("0x41682179fbf5");
printf("Десятичное: %s, 36-ричное: %s", gmp_strval($a), gmp_strval($a,36));
?>
```
