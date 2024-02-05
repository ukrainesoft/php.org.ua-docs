---
navigation:
  - function.sodium-crypto-sign-secretkey.md: « sodium\_crypto\_sign\_secretkey
  - function.sodium-crypto-sign-verify-detached.md: sodium\_crypto\_sign\_verify\_detached »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_sign\_seed\_keypair
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_sign\_seed\_keypair

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_sign\_seed\_keypair - Детермінований виведення пари ключів з одного ключа

### Опис

```methodsynopsis
sodium_crypto_sign_seed_keypair(string $seed): string
```

Скріплює початкове значення для формування секретного ключа, витягує відкритий ключ та повертає їх у вигляді пари ключів.

Функції `*_seed_keypair` ідеально підходять для створення пари ключів із паролю та солі. Використовуйте результат як `seed` для створення бажаних ключів.

### Список параметрів

`seed`

Якісь криптографічні дані. Має бути 32 байти.

### Значення, що повертаються

Ключова пара (секретний та відкритий ключі)
