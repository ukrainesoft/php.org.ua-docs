---
navigation:
  - function.sodium-crypto-sign-open.md: « sodiumcryptosignopen
  - function.sodium-crypto-sign-publickey.md: sodiumcryptosignpublickey »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptosignpublickeyfromsecretkey
---
# sodiumcryptosignpublickeyfromsecretkey

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptosignpublickeyfromsecretkey — Витягує відкритий ключ Ed25519 із секретного ключа

### Опис

```methodsynopsis
sodium_crypto_sign_publickey_from_secretkey(string $secret_key): string
```

Витягує відкритий ключ Ed25519 із секретного ключа

### Список параметрів

`secret_key`

Секретний ключ Ed25519

### Значення, що повертаються

Відкритий ключ Ed25519
