---
navigation:
  - function.sodium-crypto-kx-publickey.md: « sodiumcryptoкксpublickey
  - function.sodium-crypto-kx-seed-keypair.md: sodiumcryptoкксseedkeypair »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptoкксsecretkey
---
# sodiumcryptoкксsecretkey

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoкксsecretkey — Витягує секретний ключ із пари ключів cryptoккс

### Опис

```methodsynopsis
sodium_crypto_kx_secretkey(string $key_pair): string
```

Витягує секретний ключ із пари ключів cryptokx.

### Список параметрів

`key_pair`

Пара ключів X25519, наприклад, згенерована [sodiumcryptoкксkeypair()](function.sodium-crypto-kx-keypair.md)

### Значення, що повертаються

Секретний ключ X25519.
