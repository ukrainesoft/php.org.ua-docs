---
navigation:
  - function.sodium-crypto-core-ristretto255-scalar-mul.md: « sodiumcryptocoreristretto255scalarmul
  - function.sodium-crypto-core-ristretto255-scalar-random.md: sodiumcryptocoreristretto255scalarrandom »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptocoreristretto255scalarnegate
---
# sodiumcryptocoreristretto255scalarnegate

(PHP 8> = 8.1.0)

sodiumcryptocoreristretto255scalarnegate — Скасує скалярне значення

### Опис

```methodsynopsis
sodium_crypto_core_ristretto255_scalar_negate(string $s): string
```

Скасує скалярне значення. Доступно, починаючи з libsodium 1.0.18.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`s`

Скалярне значення.

### Значення, що повертаються

Повертає випадковий 32-байтовий рядок (string).

### Приклади

**Приклад #1 Приклад використання **sodiumcryptocoreristretto255scalarnegate()****

```php
<?php

$foo = sodium_crypto_core_ristretto255_scalar_random();

$negate = sodium_crypto_core_ristretto255_scalar_negate($foo);
$reNegate = sodium_crypto_core_ristretto255_scalar_negate($negate);

var_dump(hash_equals($foo, $reNegate));
?>
```

Результат виконання цього прикладу:

```
bool(true)
```

### Дивіться також

-   [sodiumcryptocoreristretto255scalarrandom()](function.sodium-crypto-core-ristretto255-scalar-random.md) - Генерує випадковий ключ
