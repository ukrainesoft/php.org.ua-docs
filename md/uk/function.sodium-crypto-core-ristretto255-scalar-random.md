---
navigation:
  - function.sodium-crypto-core-ristretto255-scalar-negate.md: « sodium\_crypto\_core\_ristretto255\_scalar\_negate
  - function.sodium-crypto-core-ristretto255-scalar-reduce.md: sodium\_crypto\_core\_ristretto255\_scalar\_reduce »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_core\_ristretto255\_scalar\_random
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_core\_ristretto255\_scalar\_random

(PHP 8 >= 8.1.0)

sodium\_crypto\_core\_ristretto255\_scalar\_random - Генерує випадковий ключ

### Опис

```methodsynopsis
sodium_crypto_core_ristretto255_scalar_random(): string
```

Генерує випадковий ключ. Доступно, починаючи з libsodium 1.0.18.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає випадковий 32-байтовий рядок (string).

### Приклади

**Приклад #1 Приклад використання** sodium\_crypto\_core\_ristretto255\_scalar\_random()\*\*\*\*

```php
<?php

$foo = sodium_crypto_core_ristretto255_scalar_random();
$bar = sodium_crypto_core_ristretto255_scalar_random();

$value = sodium_crypto_core_ristretto255_scalar_add($foo, $bar);
$value = sodium_crypto_core_ristretto255_scalar_sub($value, $bar);

var_dump(hash_equals($foo, $value));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```

### Дивіться також

-   [sodium\_crypto\_core\_ristretto255\_scalar\_add()](function.sodium-crypto-core-ristretto255-scalar-add.md) \- Додає скалярне значення
-   [sodium\_crypto\_core\_ristretto255\_scalar\_sub()](function.sodium-crypto-core-ristretto255-scalar-sub.md) \- Віднімає скалярне значення
