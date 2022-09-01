---
navigation:
  - function.sodium-crypto-sign-keypair.html: « sodiumcryptosignkeypair
  - function.sodium-crypto-sign-publickey-from-secretkey.html: sodiumcryptosignpublickeyfromsecretkey »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptosignopen
---
# sodiumcryptosignopen

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptosignopen — Перевірити, чи підписане повідомлення має коректний підпис

### Опис

```methodsynopsis
sodium_crypto_sign_open(string $signed_message, string $public_key): string|false
```

Перевіряє підпис, прикріплений до повідомлення, та повертає повідомлення

### Список параметрів

`signed_message`

Повідомлення, підписане [sodiumcryptosign()](function.sodium-crypto-sign.html)

`public_key`

Відкритий ключ Ed25519

### Значення, що повертаються

У разі успішного виконання повертає вихідне підписане повідомлення або **`false`** у разі виникнення помилки.
