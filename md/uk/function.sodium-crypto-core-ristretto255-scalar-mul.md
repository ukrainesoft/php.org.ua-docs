---
navigation:
  - function.sodium-crypto-core-ristretto255-scalar-invert.md: « sodium\_crypto\_core\_ristretto255\_scalar\_invert
  - function.sodium-crypto-core-ristretto255-scalar-negate.md: sodium\_crypto\_core\_ristretto255\_scalar\_negate »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_core\_ristretto255\_scalar\_mul
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_core\_ristretto255\_scalar\_mul

(PHP 8 >= 8.1.0)

sodium\_crypto\_core\_ristretto255\_scalar\_mul — Помножує скалярне значення

### Опис

```methodsynopsis
sodium_crypto_core_ristretto255_scalar_mul(string $x, string $y): string
```

Помножує скалярне значення. Доступно, починаючи з libsodium 1.0.18.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`x`

Скаляр, який представляє координату X.

`y`

Скаляр, який представляє координату Y.

### Значення, що повертаються

Повертає випадковий 32-байтовий рядок (string).

### Дивіться також

-   [sodium\_crypto\_core\_ristretto255\_scalar\_random()](function.sodium-crypto-core-ristretto255-scalar-random.md) \- Генерує випадковий ключ
