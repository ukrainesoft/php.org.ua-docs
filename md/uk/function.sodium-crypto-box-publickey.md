---
navigation:
  - function.sodium-crypto-box-publickey-from-secretkey.md: « sodiumcryptoboxpublickeyfromsecretkey
  - function.sodium-crypto-box-seal-open.md: sodiumcryptoboxsealopen »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptoboxpublickey
---
# sodiumcryptoboxpublickey

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoboxpublickey — Витягує відкритий ключ із ключової пари cryptobox

### Опис

```methodsynopsis
sodium_crypto_box_publickey(string $key_pair): string
```

Отримує лише відкритий ключ із ключової пари.

### Список параметрів

`key_pair`

Ключова пара, створена, наприклад, [sodiumcryptoboxkeypair()](function.sodium-crypto-box-keypair.md) або [sodiumcryptoboxseedkeypair()](function.sodium-crypto-box-seed-keypair.md)

### Значення, що повертаються

Відкритий ключ X25519.
