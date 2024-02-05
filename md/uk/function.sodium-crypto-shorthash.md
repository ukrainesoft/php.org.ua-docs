---
navigation:
  - function.sodium-crypto-shorthash-keygen.md: « sodium\_crypto\_shorthash\_keygen
  - function.sodium-crypto-sign-detached.md: sodium\_crypto\_sign\_detached »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_shorthash
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_shorthash

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_shorthash — Обчислює короткий хеш повідомлення та ключ

### Опис

```methodsynopsis
sodium_crypto_shorthash(string $message, string $key): string
```

**sodium\_crypto\_shorthash()** обгортає хеш-функцію під назвою SipHash-2-4, яка ідеально підходить для реалізації хеш-таблиць, які не схильні до атак відмови в обслуговуванні через колізію хешів (Hash-DoS).

SipHash-2-4 не є криптографічною хеш-функцією загального призначення.

### Список параметрів

`message`

Повідомлення, хеш якого потрібно обчислити.

`key`

Хеш-ключ.

### Значення, що повертаються
