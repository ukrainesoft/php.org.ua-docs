---
navigation:
  - function.sodium-crypto-core-ristretto255-scalar-random.md: « sodiumcryptocoreristretto255scalarrandom
  - function.sodium-crypto-core-ristretto255-scalar-sub.md: sodiumcryptocoreristretto255scalarsub »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptocoreristretto255scalarreduce
---
# sodiumcryptocoreristretto255scalarreduce

(PHP 8> = 8.1.0)

sodiumcryptocoreristretto255scalarreduce — Зменшує скалярне значення

### Опис

```methodsynopsis
sodium_crypto_core_ristretto255_scalar_reduce(string $s): string
```

Зменшує скалярне значення. Доступно, починаючи з libsodium 1.0.18.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`s`

Скалярне значення.

### Значення, що повертаються

Повертає випадковий 32-байтовий рядок (string).

### Дивіться також

-   [sodiumcryptocoreristretto255scalarrandom()](function.sodium-crypto-core-ristretto255-scalar-random.md) - Генерує випадковий ключ
