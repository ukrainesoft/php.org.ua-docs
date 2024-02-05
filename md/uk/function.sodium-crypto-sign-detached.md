---
navigation:
  - function.sodium-crypto-shorthash.md: « sodium\_crypto\_shorthash
  - function.sodium-crypto-sign-ed25519-pk-to-curve25519.md: sodium\_crypto\_sign\_ed25519\_pk\_to\_curve25519 »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_sign\_detached
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_sign\_detached

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_sign\_detached — Підписати повідомлення

### Опис

```methodsynopsis
sodium_crypto_sign_detached(string $message, string $secret_key): string
```

Підписує повідомлення секретним ключем, який можна перевірити за допомогою відкритого ключа. Функція повертає від'єднаний підпис.

### Список параметрів

`message`

Повідомлення для підписання.

`secret_key`

Секретний ключ. Дивіться [sodium\_crypto\_sign\_secretkey()](function.sodium-crypto-sign-secretkey.md)

### Значення, що повертаються

Криптографічний підпис.
