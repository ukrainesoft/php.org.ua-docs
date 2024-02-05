---
navigation:
  - function.sodium-crypto-sign-keypair.md: « sodium\_crypto\_sign\_keypair
  - function.sodium-crypto-sign-publickey-from-secretkey.md: sodium\_crypto\_sign\_publickey\_from\_secretkey »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_sign\_open
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_sign\_open

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_sign\_open — Перевірити, чи підписане повідомлення має коректний підпис

### Опис

```methodsynopsis
sodium_crypto_sign_open(string $signed_message, string $public_key): string|false
```

Перевіряє підпис, прикріплений до повідомлення, та повертає повідомлення

### Список параметрів

`signed_message`

Сообщение, подписанное[sodium\_crypto\_sign()](function.sodium-crypto-sign.md)

`public_key`

Відкритий ключ Ed25519

### Значення, що повертаються

У разі успішного виконання повертає вихідне підписане повідомлення або \*\*`false`\*\*в случае возникновения ошибки.
