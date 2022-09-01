---
navigation:
  - function.sodium-crypto-sign-publickey-from-secretkey.html: « sodiumcryptosignpublickeyfromsecretkey
  - function.sodium-crypto-sign-secretkey.html: sodiumcryptosignsecretkey »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptosignpublickey
---
# sodiumcryptosignpublickey

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptosignpublickey — Витягує відкритий ключ Ed25519 із пари ключів

### Опис

```methodsynopsis
sodium_crypto_sign_publickey(string $key_pair): string
```

Витягує відкритий ключ Ed25519 із пари ключів.

### Список параметрів

`key_pair`

Ключова пара Ed25519 (дивіться [sodiumcryptosignkeypair()](function.sodium-crypto-sign-keypair.md)

### Значення, що повертаються

Відкритий ключ Ed25519
