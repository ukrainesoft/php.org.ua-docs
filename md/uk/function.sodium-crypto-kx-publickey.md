---
navigation:
  - function.sodium-crypto-kx-keypair.md: « sodiumcryptoкксkeypair
  - function.sodium-crypto-kx-secretkey.md: sodiumcryptoкксsecretkey »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptoкксpublickey
---
# sodiumcryptoкксpublickey

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoкксpublickey — Витягує відкритий ключ із пари ключів cryptoккс

### Опис

```methodsynopsis
sodium_crypto_kx_publickey(string $key_pair): string
```

Витягує відкритий ключ із пари ключів cryptokx.

### Список параметрів

`key_pair`

Пара ключів X25519, наприклад, згенерована [sodiumcryptoкксkeypair()](function.sodium-crypto-kx-keypair.md)

### Значення, що повертаються

Відкритий ключ X25519.
