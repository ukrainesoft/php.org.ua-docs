---
navigation:
  - function.gmp-neg.md: « gmp\_neg
  - function.gmp-or.md: gmp\_or »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_nextprime
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_nextprime

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

gmp\_nextprime — Пошук наступного простого числа

### Опис

```methodsynopsis
gmp_nextprime(GMP|int|string $num): GMP
```

Шукає наступне просте число

### Список параметрів

`num`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Повертає наступне просте число більше, ніж `num` як GMP числа.

### Приклади

**Пример #1 Пример использования**gmp\_nextprime()\*\*\*\*

```php
<?php
$prime1 = gmp_nextprime(10); // ближайшее простое число, следующее за 10
$prime2 = gmp_nextprime(-1000); // ближайшее простое число, следующее за -1000

echo gmp_strval($prime1) . "\n";
echo gmp_strval($prime2) . "\n";
?>
```

Результат виконання наведеного прикладу:

```
11
2
```

### Примітки

> **Зауваження** :
> 
> Функція використовує ймовірнісний алгоритм визначення простих чисел і шанси отримати складове число надзвичайно малі.
