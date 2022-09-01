---
navigation:
  - function.sodium-crypto-sign-secretkey.html: « sodiumcryptosignsecretkey
  - function.sodium-crypto-sign-verify-detached.html: sodiumcryptosignverifydetached »
  - index.html: PHP Manual
  - ref.sodium.html: Функции Sodium
title: sodiumcryptosignseedkeypair
---
# sodiumcryptosignseedkeypair

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptosignseedkeypair - Детермінований виведення пари ключів з одного ключа

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
