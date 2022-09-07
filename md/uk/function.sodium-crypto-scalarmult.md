---
navigation:
  - function.sodium-crypto-scalarmult-ristretto255.md: « sodiumcryptoscalarmultristretto255
  - function.sodium-crypto-secretbox-keygen.md: sodiumcryptosecretboxkeygen »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptoscalarmult
---
# sodiumcryptoscalarmult

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoscalarmult — Обчислити загальний секрет на основі секретного ключа користувача та відкритого ключа іншого користувача

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
