---
navigation:
  - function.sodium-crypto-auth.md: « sodium\_crypto\_auth
  - function.sodium-crypto-box-keypair.md: sodium\_crypto\_box\_keypair »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_box\_keypair\_from\_secretkey\_and\_publickey
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_box\_keypair\_from\_secretkey\_and\_publickey

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_box\_keypair\_from\_secretkey\_and\_publickey — Створює уніфікований рядок ключової пари із секретного та відкритого ключів

### Опис

```methodsynopsis
sodium_crypto_box_keypair_from_secretkey_and_publickey(string $secret_key, string $public_key): string
```

Функция существует для удовлетворения требований API, например**crypto\_box()**. Передайте секретний ключ однієї сторони та відкритий інший ключ і ви отримаєте ключову пару для комунікації.

### Список параметрів

`secret_key`

Секретний ключ.

`public_key`

Відкритий ключ.

### Значення, що повертаються

Ключова пара X25519.
