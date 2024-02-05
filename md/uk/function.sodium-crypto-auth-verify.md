---
navigation:
  - function.sodium-crypto-auth-keygen.md: « sodium\_crypto\_auth\_keygen
  - function.sodium-crypto-auth.md: sodium\_crypto\_auth »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_auth\_verify
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_auth\_verify

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_auth\_verify — Перевіряє, чи допустимо тег для повідомлення

### Опис

```methodsynopsis
sodium_crypto_auth_verify(string $mac, string $message, string $key): bool
```

Перевіряє, що тег автентифікації дійсний для цього повідомлення та ключа.

На відміну від цифрових підписів (наприклад, [sodium\_crypto\_sign\_verify\_detached()](function.sodium-crypto-sign-verify-detached.md)), будь-яка сторона, здатна перевірити повідомлення, також здатна перевірити справжність своїх власних повідомлень. (Отже, симетрична автентифікація.)

### Список параметрів

`mac`

Тег аутентифікації, створений [sodium\_crypto\_auth()](function.sodium-crypto-auth.md)

`message`

Повідомлення

`key`

Ключ аутентифікації

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
