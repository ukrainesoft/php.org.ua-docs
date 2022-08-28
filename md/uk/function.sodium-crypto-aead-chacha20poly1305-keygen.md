Створює випадковий ключ ChaCha20-Poly1305

-   [« sodium\_crypto\_aead\_chacha20poly1305\_ietf\_keygen](function.sodium-crypto-aead-chacha20poly1305-ietf-keygen.html)
    
-   [sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_decrypt »](function.sodium-crypto-aead-xchacha20poly1305-ietf-decrypt.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Створює випадковий ключ ChaCha20-Poly1305
    

# sodiumcryptoaeadchacha20poly1305keygen

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoaeadchacha20poly1305keygen — Створює випадковий ключ ChaCha20-Poly1305

### Опис

```methodsynopsis
sodium_crypto_aead_chacha20poly1305_keygen(): string
```

Створює випадковий ключ для використання в [sodium\_crypto\_aead\_chacha20poly1305\_encrypt()](function.sodium-crypto-aead-chacha20poly1305-encrypt.html) і [sodium\_crypto\_aead\_chacha20poly1305\_decrypt()](function.sodium-crypto-aead-chacha20poly1305-decrypt.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає 256-бітний випадковий ключ.