---
navigation:
  - function.sodium-crypto-box-secretkey.md: « sodium\_crypto\_box\_secretkey
  - function.sodium-crypto-box.md: sodium\_crypto\_box »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_box\_seed\_keypair
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_box\_seed\_keypair

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_box\_seed\_keypair - Детерміністичний висновок ключової пари з одного ключа

### Опис

```methodsynopsis
sodium_crypto_box_seed_keypair(string $seed): string
```

Скріплює початкове значення для формування секретного ключа, витягує відкритий ключ та повертає їх у вигляді пари ключів.

Функції `*_seed_keypair` ідеально підходять для створення пари ключів із паролю та солі. Використовуйте результат як `seed` для створення бажаних ключів.

### Список параметрів

`seed`

Якісь криптографічні дані. Має бути 32 байти.

### Значення, що повертаються

Ключова пара X25519 (секретний та відкритий ключі).
