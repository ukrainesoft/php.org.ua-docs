Перевіряє, потім розшифровує за допомогою ChaCha20-Poly1305

-   [« sodium\_crypto\_aead\_aes256gcm\_keygen](function.sodium-crypto-aead-aes256gcm-keygen.html)
    
-   [sodium\_crypto\_aead\_chacha20poly1305\_encrypt »](function.sodium-crypto-aead-chacha20poly1305-encrypt.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Перевіряє, потім розшифровує за допомогою ChaCha20-Poly1305
    

# sodiumcryptoaeadchacha20poly1305decrypt

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoaeadchacha20poly1305decrypt — Перевіряє, потім розшифровує за допомогою ChaCha20-Poly1305

### Опис

```methodsynopsis
sodium_crypto_aead_chacha20poly1305_decrypt(    string $ciphertext,    string $additional_data,    string $nonce,    string $key): string|false
```

Перевіряє, потім розшифровує за допомогою ChaCha20-Poly1305

### Список параметрів

`ciphertext`

Має бути у форматі, наданому [sodium\_crypto\_aead\_chacha20poly1305\_encrypt()](function.sodium-crypto-aead-chacha20poly1305-encrypt.html) (Зашифрований текст та тег, об'єднані).

`additional_data`

Додаткові перевірені дані. Це використовується при перевірці автентичності, доданого до зашифрованого тексту, але він не шифрується і не зберігається в зашифрованому тексті.

`nonce`

Номер, який потрібно використовувати лише один раз для кожного повідомлення. Довжина 8 байт.

`key`

Ключ шифрування (256 біт).

### Значення, що повертаються

У разі успішного виконання повертає текст або **`false`** у разі виникнення помилки.