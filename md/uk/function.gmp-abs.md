---
navigation:
  - ref.gmp.md: « GMP Функції
  - function.gmp-add.md: gmp\_add »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_abs
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_abs

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_abs - Абсолютна величина

### Опис

```methodsynopsis
gmp_abs(GMP|int|string $num): GMP
```

Отримання абсолютної величини числа.

### Список параметрів

`num`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Повертає абсолютну величину аргументу `num`, як GMP числа.

### Приклади

**Приклад #1 Приклад використання** gmp\_abs()\*\*\*\*

```php
<?php
     $abs1 = gmp_abs("274982683358");
     $abs2 = gmp_abs("-274982683358");

     echo gmp_strval($abs1) . "\n";
     echo gmp_strval($abs2) . "\n";
     ?>
```

Результат виконання наведеного прикладу:

```
274982683358
     274982683358
```
