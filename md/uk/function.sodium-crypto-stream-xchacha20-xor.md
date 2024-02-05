---
navigation:
  - function.sodium-crypto-stream-xchacha20-xor-ic.md: « sodium\_crypto\_stream\_xchacha20\_xor\_ic
  - function.sodium-crypto-stream-xchacha20.md: sodium\_crypto\_stream\_xchacha20 »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_stream\_xchacha20\_xor
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_stream\_xchacha20\_xor

(PHP 8 >= 8.1.0)

sodium\_crypto\_stream\_xchacha20\_xor — Шифрує повідомлення, використовуючи одноразовий номер та секретний ключ (без автентифікації)

### Опис

```methodsynopsis
sodium_crypto_stream_xchacha20_xor(string $message, string $nonce, string $key): string
```

Шифрує повідомлення `message`, використовуючи одноразовий номер `nonce` та секретний ключ `key` (Без аутентифікації).

**Застереження**

Це шифрування не автентифікується і не запобігає атакам з вибраним зашифрованим текстом. Обов'язково об'єднайте зашифрований текст із кодом автентифікації повідомлення (Message Authentication Code), наприклад, за допомогою функції [sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_encrypt()](function.sodium-crypto-aead-xchacha20poly1305-ietf-encrypt.md) або [sodium\_crypto\_auth()](function.sodium-crypto-auth.md)

### Список параметрів

`message`

Повідомлення для шифрування.

`nonce`

24-байтовий одноразовий номер.

`key`

Ключ, можливо, згенерований за допомогою функції [sodium\_crypto\_stream\_xchacha20\_keygen()](function.sodium-crypto-stream-xchacha20-keygen.md)

### Значення, що повертаються

Зашифровані повідомлення.

### Дивіться також

-   [sodium\_crypto\_stream\_xchacha20\_xor\_ic()](function.sodium-crypto-stream-xchacha20-xor-ic.md) \- Шифрує повідомлення, використовуючи неясний код та секретний ключ (без автентифікації)
