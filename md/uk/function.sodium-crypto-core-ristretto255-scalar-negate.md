---
navigation:
  - function.sodium-crypto-core-ristretto255-scalar-mul.md: « sodium\_crypto\_core\_ristretto255\_scalar\_mul
  - function.sodium-crypto-core-ristretto255-scalar-random.md: sodium\_crypto\_core\_ristretto255\_scalar\_random »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_core\_ristretto255\_scalar\_negate
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_core\_ristretto255\_scalar\_negate

(PHP 8 >= 8.1.0)

sodium\_crypto\_core\_ristretto255\_scalar\_negate — Скасує скалярне значення

### Опис

```methodsynopsis
sodium_crypto_core_ristretto255_scalar_negate(string $s): string
```

Скасує скалярне значення. Доступно, починаючи з libsodium 1.0.18.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`s`

Скалярне значення.

### Значення, що повертаються

Повертає випадковий 32-байтовий рядок (string).

### Приклади

**Пример #1 Пример использования**sodium\_crypto\_core\_ristretto255\_scalar\_negate()\*\*\*\*

```php
<?php

$foo = sodium_crypto_core_ristretto255_scalar_random();

$negate = sodium_crypto_core_ristretto255_scalar_negate($foo);
$reNegate = sodium_crypto_core_ristretto255_scalar_negate($negate);

var_dump(hash_equals($foo, $reNegate));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```

### Дивіться також

-   [sodium\_crypto\_core\_ristretto255\_scalar\_random()](function.sodium-crypto-core-ristretto255-scalar-random.md) \- Генерує випадковий ключ
