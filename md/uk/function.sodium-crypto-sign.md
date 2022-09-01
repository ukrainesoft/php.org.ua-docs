---
navigation:
  - function.sodium-crypto-sign-verify-detached.html: « sodiumcryptosignverifydetached
  - function.sodium-crypto-stream-keygen.html: sodiumcryptostreamkeygen »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptosign
---
# sodiumcryptosign

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptosign — Підписати повідомлення

### Опис

```methodsynopsis
sodium_crypto_sign(string $message, string $secret_key): string
```

Підписує повідомлення секретним ключем, який можна перевірити за допомогою відкритого ключа. Функція підписує повідомлення. Подробиці у розділі [sodiumcryptosigndetached()](function.sodium-crypto-sign-detached.html) для окремих підписів.

### Список параметрів

`message`

Повідомлення для підпису.

`secret_key`

Секретний ключ. Дивіться [sodiumcryptosignsecretkey()](function.sodium-crypto-sign-secretkey.html)

### Значення, що повертаються

Підписане повідомлення (не зашифроване).
