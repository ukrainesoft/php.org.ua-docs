Створює випадковий ключ AES-256-GCM

-   [« sodium\_crypto\_aead\_aes256gcm\_is\_available](function.sodium-crypto-aead-aes256gcm-is-available.html)
    
-   [sodium\_crypto\_aead\_chacha20poly1305\_decrypt »](function.sodium-crypto-aead-chacha20poly1305-decrypt.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Створює випадковий ключ AES-256-GCM
    

# sodiumcryptoaeadaes256gcmkeygen

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoaeadaes256gcmkeygen — Створює випадковий ключ AES-256-GCM

### Опис

```methodsynopsis
sodium_crypto_aead_aes256gcm_keygen(): string
```

Створює випадковий ключ для використання в [sodium\_crypto\_aead\_aes256gcm\_encrypt()](function.sodium-crypto-aead-aes256gcm-encrypt.html) і [sodium\_crypto\_aead\_aes256gcm\_decrypt()](function.sodium-crypto-aead-aes256gcm-decrypt.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає 256-бітний випадковий ключ.