---
navigation:
  - function.sodium-crypto-sign-ed25519-sk-to-curve25519.md: « sodium\_crypto\_sign\_ed25519\_sk\_to\_curve25519
  - function.sodium-crypto-sign-keypair.md: sodium\_crypto\_sign\_keypair »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_sign\_keypair\_from\_secretkey\_and\_publickey
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_sign\_keypair\_from\_secretkey\_and\_publickey

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_sign\_keypair\_from\_secretkey\_and\_publickey — Об'єднує секретний ключ та відкритий ключ разом

### Опис

```methodsynopsis
sodium_crypto_sign_keypair_from_secretkey_and_publickey(string $secret_key, string $public_key): string
```

Об'єднує секретний ключ та відкритий ключ разом.

### Список параметрів

`secret_key`

Секретний ключ Ed25519

`public_key`

Відкритий ключ Ed25519

### Значення, що повертаються

Ключова пара
