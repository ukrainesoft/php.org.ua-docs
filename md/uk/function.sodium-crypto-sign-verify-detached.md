---
navigation:
  - function.sodium-crypto-sign-seed-keypair.md: « sodium\_crypto\_sign\_seed\_keypair
  - function.sodium-crypto-sign.md: sodium\_crypto\_sign »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_sign\_verify\_detached
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_sign\_verify\_detached

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_sign\_verify\_detached — Перевірити підпис для повідомлення

### Опис

```methodsynopsis
sodium_crypto_sign_verify_detached(string $signature, string $message, string $public_key): bool
```

Перевіряє підпис для повідомлення

### Список параметрів

`signature`

Криптографічний підпис, отриманий за допомогою [sodium\_crypto\_sign\_detached()](function.sodium-crypto-sign-detached.md)

`message`

Перевірене повідомлення

`public_key`

Відкритий ключ ed25519

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
