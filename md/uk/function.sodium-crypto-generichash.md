---
navigation:
  - function.sodium-crypto-generichash-update.html: « sodiumcryptogenerichashupdate
  - function.sodium-crypto-kdf-derive-from-key.html: sodiumcryptokdfderivefromkey »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptogenerichash
---
# sodiumcryptogenerichash

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptogenerichash — Отримати повідомлення хеша

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

Криптографічний хеш як необроблених байтів. Якщо бажаний висновок у шістнадцятковому коді, результат можна передати в [sodiumbin2hex()](function.sodium-bin2hex.md)
