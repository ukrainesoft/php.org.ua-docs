---
navigation:
  - function.sodium-crypto-scalarmult-base.md: « sodium\_crypto\_scalarmult\_base
  - function.sodium-crypto-scalarmult-ristretto255.md: sodium\_crypto\_scalarmult\_ristretto255 »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_scalarmult\_ristretto255\_base
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_scalarmult\_ristretto255\_base

(PHP 8 >= 8.1.1)

sodium\_crypto\_scalarmult\_ristretto255\_base — Обчислює відкритий ключ із закритого ключа

### Опис

```methodsynopsis
sodium_crypto_scalarmult_ristretto255_base(string $n): string
```

З огляду на закритий ключ обчислює відповідний відкритий ключ. Доступно, починаючи з libsodium 1.0.18.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`n`

Закритий ключ.

### Значення, що повертаються

Повертає випадковий 32-байтовий рядок (string).

### Дивіться також

-   [sodium\_crypto\_scalarmult\_ristretto255()](function.sodium-crypto-scalarmult-ristretto255.md) \- обчислює загальний секрет
