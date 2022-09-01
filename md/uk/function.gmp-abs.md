---
navigation:
  - ref.gmp.html: « GMP Функції
  - function.gmp-add.html: gmpadd »
  - index.html: PHP Manual
  - ref.gmp.html: GMP Функції
title: gmpabs
---
# gmpabs

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmpabs - Абсолютна величина

### Опис

```methodsynopsis
gmp_abs(GMP|int|string $num): GMP
```

Отримання абсолютної величини числа.

### Список параметрів

`num`

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Повертає абсолютну величину аргументу `num`, як GMP числа.

### Приклади

**Приклад #1 Приклад використання **gmpabs()****

```php
<?php
     $abs1 = gmp_abs("274982683358");
     $abs2 = gmp_abs("-274982683358");

     echo gmp_strval($abs1) . "\n";
     echo gmp_strval($abs2) . "\n";
     ?>
```

Результат виконання цього прикладу:

```
274982683358
     274982683358
```
