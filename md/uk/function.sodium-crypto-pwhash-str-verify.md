---
navigation:
  - function.sodium-crypto-pwhash-str-needs-rehash.md: « sodium\_crypto\_pwhash\_str\_needs\_rehash
  - function.sodium-crypto-pwhash-str.md: sodium\_crypto\_pwhash\_str »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_pwhash\_str\_verify
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_pwhash\_str\_verify

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_pwhash\_str\_verify — Перевіряє, чи пароль відповідає хешу

### Опис

```methodsynopsis
sodium_crypto_pwhash_str_verify(string $hash, string $password): bool
```

Перевіряє, що хеш пароля, створений [sodium\_crypto\_pwhash\_str()](function.sodium-crypto-pwhash-str.md)відповідає заданому паролю. Зверніть увагу, що в цій функції порядок аргументів не відповідає порядку аргументів у схожій функції [password\_verify()](function.password-verify.md)

### Список параметрів

`hash`

Хеш, створений функцією [password\_hash()](function.password-hash.md)

`password`

Користувальницький пароль.

### Значення, що повертаються

Повертає **`true`**, якщо пароль відповідає хешу, та **`false`**, якщо ні.

### Примітки

> **Зауваження** :
> 
> Хеші обчислюються за допомогою алгоритму Argon2ID, який добре протистоїть обом видам атак: GPU та атакам по сторонньому каналу.

### Дивіться також

-   [sodium\_crypto\_pwhash\_str()](function.sodium-crypto-pwhash-str.md) \- Отримати ASCII-кодований хеш
-   [password\_hash()](function.password-hash.md) \- Створює хеш пароля
-   [password\_verify()](function.password-verify.md) \- Перевіряє, чи пароль хешу відповідає
