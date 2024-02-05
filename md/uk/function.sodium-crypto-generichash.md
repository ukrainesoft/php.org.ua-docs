---
navigation:
  - function.sodium-crypto-generichash-update.md: « sodium\_crypto\_generichash\_update
  - function.sodium-crypto-kdf-derive-from-key.md: sodium\_crypto\_kdf\_derive\_from\_key »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_generichash
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_generichash

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_generichash — Отримати повідомлення хеша

### Опис

```methodsynopsis
sodium_crypto_generichash(string $message, string $key = "", int $length = SODIUM_CRYPTO_GENERICHASH_BYTES): string
```

Хешує повідомлення за допомогою BLAKE2b.

### Список параметрів

`message`

Хешені повідомлення.

`key`

(Необов'язковий) криптографічний ключ. Він виконує ту ж функцію, що й ключ HMAC, але використовується як зарезервований розділ внутрішнього стану BLAKE2.

`length`

Розмір виводу.

### Значення, що повертаються

Криптографічний хеш як необроблених байтів. Якщо бажаний висновок у шістнадцятковому коді, результат можна передати в [sodium\_bin2hex()](function.sodium-bin2hex.md)
