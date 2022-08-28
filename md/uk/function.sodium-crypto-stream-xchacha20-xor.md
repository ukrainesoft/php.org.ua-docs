Шифрує повідомлення, використовуючи одноразовий номер та секретний ключ (без автентифікації)

-   [« sodium\_crypto\_stream\_xchacha20\_keygen](function.sodium-crypto-stream-xchacha20-keygen.html)
    
-   [sodium\_crypto\_stream\_xchacha20 »](function.sodium-crypto-stream-xchacha20.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Шифрує повідомлення, використовуючи одноразовий номер та секретний ключ (без автентифікації)
    

# sodiumcryptostreamxchacha20xor

(PHP 8> = 8.1.0)

sodiumcryptostreamxchacha20xor — Шифрує повідомлення, використовуючи одноразовий номер та секретний ключ (без автентифікації)

### Опис

```methodsynopsis
sodium_crypto_stream_xchacha20_xor(string $message, string $nonce, string $key): string
```

Шифрує повідомлення `message`, використовуючи одноразовий номер `nonce` та секретний ключ `key` (Без аутентифікації).

**Застереження**

Це шифрування не автентифікується і не запобігає атакам з вибраним зашифрованим текстом. Обов'язково об'єднайте зашифрований текст із кодом автентифікації повідомлення (Message Authentication Code), наприклад, за допомогою функції [sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_encrypt()](function.sodium-crypto-aead-xchacha20poly1305-ietf-encrypt.html) або [sodium\_crypto\_auth()](function.sodium-crypto-auth.html)

### Список параметрів

`message`

Повідомлення для шифрування.

`nonce`

24-байтовий одноразовий номер.

`key`

Ключ, можливо, згенерований за допомогою функції [sodium\_crypto\_stream\_xchacha20\_keygen()](function.sodium-crypto-stream-xchacha20-keygen.html)

### Значення, що повертаються

Зашифровані повідомлення.