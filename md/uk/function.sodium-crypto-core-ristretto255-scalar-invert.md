---
navigation:
  - function.sodium-crypto-core-ristretto255-scalar-complement.md: « sodiumcryptocoreristretto255scalarcomplement
  - function.sodium-crypto-core-ristretto255-scalar-mul.md: sodiumcryptocoreristretto255scalarmul »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptocoreristretto255scalarinvert
---
# sodiumcryptocoreristretto255scalarinvert

(PHP 8> = 8.1.0)

sodiumcryptocoreristretto255scalarinvert — Інвертує скалярне значення

### Опис

```methodsynopsis
sodium_crypto_core_ristretto255_scalar_invert(string $s): string
```

Інвертує скалярне значення. Доступно, починаючи з libsodium 1.0.18.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`s`

Скалярне значення.

### Значення, що повертаються

Повертає випадковий 32-байтовий рядок (string).

### Приклади

**Приклад #1 Приклад використання **sodiumcryptocoreristretto255scalarinvert()****

```php
<?php

$foo = sodium_crypto_core_ristretto255_scalar_random();

$inverted = sodium_crypto_core_ristretto255_scalar_invert($foo);
$reInverted = sodium_crypto_core_ristretto255_scalar_invert($inverted);

var_dump(hash_equals($foo, $reInverted));
?>
```

Результат виконання цього прикладу:

```
bool(true)
```

### Дивіться також

-   [sodiumcryptocoreristretto255scalarrandom()](function.sodium-crypto-core-ristretto255-scalar-random.md) - Генерує випадковий ключ
