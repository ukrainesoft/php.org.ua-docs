---
navigation:
  - function.sodium-crypto-sign-publickey.html: « sodiumcryptosignpublickey
  - function.sodium-crypto-sign-seed-keypair.html: sodiumcryptosignseedkeypair »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptosignsecretkey
---
# sodiumcryptosignsecretkey

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptosignsecretkey — Витягує секретний ключ Ed25519 із пари ключів

### Опис

```methodsynopsis
sodium_crypto_sign_secretkey(string $key_pair): string
```

Витягує секретний ключ Ed25519 із пари ключів

### Список параметрів

`key_pair`

Ключова пара Ed25519 (дивіться [sodiumcryptosignkeypair()](function.sodium-crypto-sign-keypair.md)

### Значення, що повертаються

Секретний ключ Ed25519
