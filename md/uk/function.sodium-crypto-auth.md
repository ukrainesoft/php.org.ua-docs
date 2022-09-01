---
navigation:
  - function.sodium-crypto-auth-verify.html: « sodiumcryptoauthverify
  - function.sodium-crypto-box-keypair-from-secretkey-and-publickey.html: sodiumcryptoboxkeypairfromsecretkeyandpublickey »
  - index.html: PHP Manual
  - ref.sodium.html: Функции Sodium
title: sodiumcryptoauth
---
# sodiumcryptoauth

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoauth — Визначити тег для повідомлення

### Опис

```methodsynopsis
sodium_crypto_auth(string $message, string $key): string
```

Симетрична автентифікація повідомлення за допомогою **sodiumcryptoauth()** забезпечує цілісність, але з конфіденційність.

На відміну від цифрових підписів (наприклад, [sodiumcryptosigndetached()](function.sodium-crypto-sign-detached.html)), будь-яка сторона, здатна перевірити повідомлення, також здатна перевірити справжність своїх власних повідомлень. (Отже, симетрична автентифікація.)

### Список параметрів

`message`

Повідомлення, яке ви маєте намір підтвердити.

`key`

Ключ аутентифікації

### Значення, що повертаються

Тег аутентифікації
