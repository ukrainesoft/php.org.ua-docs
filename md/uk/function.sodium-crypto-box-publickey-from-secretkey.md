---
navigation:
  - function.sodium-crypto-box-open.md: « sodium\_crypto\_box\_open
  - function.sodium-crypto-box-publickey.md: sodium\_crypto\_box\_publickey »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_box\_publickey\_from\_secretkey
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_box\_publickey\_from\_secretkey

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_box\_publickey\_from\_secretkey — Обчислює відкритий ключ із секретного ключа

### Опис

```methodsynopsis
sodium_crypto_box_publickey_from_secretkey(string $secret_key): string
```

З огляду на секретний ключ обчислює відповідний відкритий ключ.

Працює тільки з типом ключів, призначеним для використання з **crypto\_box()** (який використовує еліптичну криву Діффі-Хеллмана на кривій Монтгомері, Curve25519; скорочено X25519), а не **crypto\_sign()** (який використовує алгоритм цифрового підпису Едвардса по кривій Едвардса з відповідними параметрами; скорочено Ed25519).

### Список параметрів

`secret_key`

Секретний ключ X25519

### Значення, що повертаються

Відкритий ключ X25519.
