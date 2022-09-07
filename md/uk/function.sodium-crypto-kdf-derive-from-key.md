---
navigation:
  - function.sodium-crypto-generichash.md: « sodiumcryptogenerichash
  - function.sodium-crypto-kdf-keygen.md: sodiumcryptokdfkeygen »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptokdfderivefromkey
---
# sodiumcryptokdfderivefromkey

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptokdfderivefromkey — Витягти підрозділ

### Опис

```methodsynopsis
sodium_crypto_kdf_derive_from_key(    int $subkey_length,    int $subkey_id,    string $context,    string $key): string
```

Отримує підрозділ із кореневого ключа та додаткового контексту.

Схожа на[hashhkdf()](function.hash-hkdf.md)

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
