---
navigation:
  - function.sodium-crypto-core-ristretto255-scalar-complement.md: « sodium\_crypto\_core\_ristretto255\_scalar\_complement
  - function.sodium-crypto-core-ristretto255-scalar-mul.md: sodium\_crypto\_core\_ristretto255\_scalar\_mul »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_core\_ristretto255\_scalar\_invert
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_core\_ristretto255\_scalar\_invert

(PHP 8 >= 8.1.0)

sodium\_crypto\_core\_ristretto255\_scalar\_invert — Інвертує скалярне значення

### Опис

```methodsynopsis
sodium_crypto_core_ristretto255_scalar_invert(string $s): string
```

Інвертує скалярне значення. Доступно, починаючи з libsodium 1.0.18.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`s`

Скалярне значення.

### Значення, що повертаються

Повертає випадковий 32-байтовий рядок (string).

### Приклади

**Приклад #1 Приклад використання** sodium\_crypto\_core\_ristretto255\_scalar\_invert()\*\*\*\*

```php
<?php

$foo = sodium_crypto_core_ristretto255_scalar_random();

$inverted = sodium_crypto_core_ristretto255_scalar_invert($foo);
$reInverted = sodium_crypto_core_ristretto255_scalar_invert($inverted);

var_dump(hash_equals($foo, $reInverted));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```

### Дивіться також

-   [sodium\_crypto\_core\_ristretto255\_scalar\_random()](function.sodium-crypto-core-ristretto255-scalar-random.md) \- Генерує випадковий ключ
