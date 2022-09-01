---
navigation:
  - function.sodium-crypto-core-ristretto255-scalar-invert.html: « sodiumcryptocoreristretto255scalarinvert
  - function.sodium-crypto-core-ristretto255-scalar-negate.html: sodiumcryptocoreristretto255scalarnegate »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptocoreristretto255scalarmul
---
# sodiumcryptocoreristretto255scalarmul

(PHP 8> = 8.1.0)

sodiumcryptocoreristretto255scalarmul — Помножує скалярне значення

### Опис

```methodsynopsis
sodium_crypto_core_ristretto255_scalar_mul(string $x, string $y): string
```

Помножує скалярне значення. Доступно, починаючи з libsodium 1.0.18.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`x`

Скаляр, який представляє координату X.

`y`

Скаляр, який представляє координату Y.

### Значення, що повертаються

Повертає випадковий 32-байтовий рядок (string).

### Дивіться також

-   [sodiumcryptocoreristretto255scalarrandom()](function.sodium-crypto-core-ristretto255-scalar-random.md) - Генерує випадковий ключ
