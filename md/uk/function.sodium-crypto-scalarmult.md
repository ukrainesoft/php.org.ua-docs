---
navigation:
  - function.sodium-crypto-scalarmult-ristretto255.md: « sodium\_crypto\_scalarmult\_ristretto255
  - function.sodium-crypto-secretbox-keygen.md: sodium\_crypto\_secretbox\_keygen »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_scalarmult
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_scalarmult

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_scalarmult — Обчислити загальний секрет на основі секретного ключа користувача та відкритого ключа іншого користувача

### Опис

```methodsynopsis
sodium_crypto_scalarmult(string $n, string $p): string
```

Еліптична крива Діффі-Хеллмана. Обчислює скаляр n, помножений на точку p на еліптичній кривій.

### Список параметрів

`n`

скаляр, який зазвичай є секретним ключем

`p`

точка (координата x), яка зазвичай є відкритим ключем

### Значення, що повертаються

32-байтовий випадковий рядок.
