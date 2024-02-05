---
navigation:
  - function.sodium-crypto-generichash.md: « sodium\_crypto\_generichash
  - function.sodium-crypto-kdf-keygen.md: sodium\_crypto\_kdf\_keygen »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_kdf\_derive\_from\_key
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_kdf\_derive\_from\_key

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_kdf\_derive\_from\_key — Витягти підрозділ

### Опис

```methodsynopsis
sodium_crypto_kdf_derive_from_key(    int $subkey_length,    int $subkey_id,    string $context,    string $key): string
```

Отримує підрозділ із кореневого ключа та додаткового контексту.

Схожа на[hash\_hkdf()](function.hash-hkdf.md)

### Список параметрів

`subkey_length`

Довжина ключа, що повертається (в байтах)

`subkey_id`

Повернути підключення n із заданого кореневого ключа. Корисно для пошуку.

`context`

Контекст, що залежить від програми.

`key`

Кореневий ключ, з якого отримано підключення.

### Значення, що повертаються

Рядок псевдовипадкових (необроблених двійкових) байтів.
