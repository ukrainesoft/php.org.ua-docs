---
navigation:
  - function.sodium-crypto-core-ristretto255-random.md: « sodiumcryptocoreristretto255random
  - function.sodium-crypto-core-ristretto255-scalar-complement.md: sodiumcryptocoreristretto255scalarcomplement »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptocoreristretto255scalaradd
---
# sodiumcryptocoreristretto255scalaradd

(PHP 8> = 8.1.0)

sodiumcryptocoreristretto255scalaradd — Додає скалярне значення

### Опис

```methodsynopsis
sodium_crypto_core_ristretto255_scalar_add(string $x, string $y): string
```

Додає елемент `y` до `x`. Доступно, починаючи з libsodium 1.0.18.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`x`

Скаляр, який представляє координату X.

`y`

Скаляр, який представляє координату Y.

### Значення, що повертаються

Повертає випадковий 32-байтовий рядок (string).

### Приклади

**Приклад #1 Приклад використання **sodiumcryptocoreristretto255scalaradd()****

```php
<?php

$foo = sodium_crypto_core_ristretto255_scalar_random();
$bar = sodium_crypto_core_ristretto255_scalar_random();

$value = sodium_crypto_core_ristretto255_scalar_add($foo, $bar);
$value = sodium_crypto_core_ristretto255_scalar_sub($value, $bar);

var_dump(hash_equals($foo, $value));
?>
```

Результат виконання цього прикладу:

```
bool(true)
```

### Дивіться також

-   [sodiumcryptocoreristretto255scalarrandom()](function.sodium-crypto-core-ristretto255-scalar-random.md) - Генерує випадковий ключ
-   [sodiumcryptocoreristretto255scalarsub()](function.sodium-crypto-core-ristretto255-scalar-sub.md) - Віднімає скалярне значення
