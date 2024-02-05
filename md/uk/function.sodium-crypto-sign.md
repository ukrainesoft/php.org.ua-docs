---
navigation:
  - function.sodium-crypto-sign-verify-detached.md: « sodium\_crypto\_sign\_verify\_detached
  - function.sodium-crypto-stream-keygen.md: sodium\_crypto\_stream\_keygen »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_sign
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_sign

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_sign — Підписати повідомлення

### Опис

```methodsynopsis
sodium_crypto_sign(string $message, string $secret_key): string
```

Підписує повідомлення секретним ключем, який можна перевірити за допомогою відкритого ключа. Функція підписує повідомлення. Подробиці у розділі [sodium\_crypto\_sign\_detached()](function.sodium-crypto-sign-detached.md) для окремих підписів.

### Список параметрів

`message`

Повідомлення для підпису.

`secret_key`

Секретний ключ. Дивіться [sodium\_crypto\_sign\_secretkey()](function.sodium-crypto-sign-secretkey.md)

### Значення, що повертаються

Підписане повідомлення (не зашифроване).
