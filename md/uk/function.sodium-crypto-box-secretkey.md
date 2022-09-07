---
navigation:
  - function.sodium-crypto-box-seal.md: « sodiumcryptoboxseal
  - function.sodium-crypto-box-seed-keypair.md: sodiumcryptoboxseedkeypair »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptoboxsecretkey
---
# sodiumcryptoboxsecretkey

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoboxsecretkey — Витягує секретний ключ із ключової пари cryptobox

### Опис

```methodsynopsis
sodium_crypto_box_secretkey(string $key_pair): string
```

Отримує лише секретний ключ для цієї ключової пари.

### Список параметрів

`key_pair`

Пара ключів, створена, наприклад, [sodiumcryptoboxkeypair()](function.sodium-crypto-box-keypair.md) або [sodiumcryptoboxseedkeypair()](function.sodium-crypto-box-seed-keypair.md)

### Значення, що повертаються

Секретний ключ X25519.
