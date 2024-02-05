---
navigation:
  - function.sodium-crypto-scalarmult-ristretto255-base.md: « sodium\_crypto\_scalarmult\_ristretto255\_base
  - function.sodium-crypto-scalarmult.md: sodium\_crypto\_scalarmult »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_scalarmult\_ristretto255
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_scalarmult\_ristretto255

(PHP 8 >= 8.1.1)

sodium\_crypto\_scalarmult\_ristretto255 - Обчислює загальний секрет

### Опис

```methodsynopsis
sodium_crypto_scalarmult_ristretto255(string $n, string $p): string
```

Обчислює скаляр `n`, помножений на крапку `p`. Доступно, починаючи з libsodium 1.0.18.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`n`

Скаляр, який зазвичай є закритим ключем.

`p`

Крапка (x-координата), яка зазвичай є відкритим ключем.

### Значення, що повертаються

Повертає випадковий 32-байтовий рядок (string).

### Дивіться також

-   [sodium\_crypto\_scalarmult\_ristretto255\_base()](function.sodium-crypto-scalarmult-ristretto255-base.md) \- Обчислює відкритий ключ із закритого ключа
