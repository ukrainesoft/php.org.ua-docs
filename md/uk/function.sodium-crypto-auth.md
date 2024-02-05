---
navigation:
  - function.sodium-crypto-auth-verify.md: « sodium\_crypto\_auth\_verify
  - function.sodium-crypto-box-keypair-from-secretkey-and-publickey.md: sodium\_crypto\_box\_keypair\_from\_secretkey\_and\_publickey »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_auth
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_auth

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_auth — Визначити тег для повідомлення

### Опис

```methodsynopsis
sodium_crypto_auth(string $message, string $key): string
```

Симетрична автентифікація повідомлення за допомогою **sodium\_crypto\_auth()** забезпечує цілісність, але з конфіденційність.

На відміну від цифрових підписів (наприклад, [sodium\_crypto\_sign\_detached()](function.sodium-crypto-sign-detached.md)), будь-яка сторона, здатна перевірити повідомлення, також здатна перевірити справжність своїх власних повідомлень. (Отже, симетрична автентифікація.)

### Список параметрів

`message`

Повідомлення, яке ви маєте намір підтвердити.

`key`

Ключ аутентифікації

### Значення, що повертаються

Тег аутентифікації
