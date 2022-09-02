---
navigation:
  - function.sodium-crypto-stream-xchacha20-keygen.md: « sodiumcryptostreamxchacha20keygen
  - function.sodium-crypto-stream-xchacha20.md: sodiumcryptostreamxchacha20 »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptostreamxchacha20xor
---
# sodiumcryptostreamxchacha20xor

(PHP 8> = 8.1.0)

sodiumcryptostreamxchacha20xor — Шифрує повідомлення, використовуючи одноразовий номер та секретний ключ (без автентифікації)

### Опис

```methodsynopsis
sodium_crypto_stream_xchacha20_xor(string $message, string $nonce, string $key): string
```

Шифрує повідомлення `message`, використовуючи одноразовий номер `nonce` та секретний ключ `key` (Без аутентифікації).

**Застереження**

Це шифрування не автентифікується і не запобігає атакам з вибраним зашифрованим текстом. Обов'язково об'єднайте зашифрований текст із кодом автентифікації повідомлення (Message Authentication Code), наприклад, за допомогою функції [sodiumcryptoaeadxchacha20poly1305ietfencrypt()](function.sodium-crypto-aead-xchacha20poly1305-ietf-encrypt.md) або [sodiumcryptoauth()](function.sodium-crypto-auth.md)

### Список параметрів

`message`

Повідомлення для шифрування.

`nonce`

24-байтовий одноразовий номер.

`key`

Ключ, можливо, згенерований за допомогою функції [sodiumcryptostreamxchacha20keygen()](function.sodium-crypto-stream-xchacha20-keygen.md)

### Значення, що повертаються

Зашифровані повідомлення.
