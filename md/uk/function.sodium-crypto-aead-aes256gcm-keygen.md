Створює випадковий ключ AES-256-GCM

-   [« sodiumcryptoaeadaes256gcmісavailable](function.sodium-crypto-aead-aes256gcm-is-available.html)
    
-   [sodiumcryptoaeadchacha20poly1305decrypt »](function.sodium-crypto-aead-chacha20poly1305-decrypt.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Sodium](ref.sodium.md)
    
-   Створює випадковий ключ AES-256-GCM
    

# sodiumcryptoaeadaes256gcmkeygen

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoaeadaes256gcmkeygen — Створює випадковий ключ AES-256-GCM

### Опис

```methodsynopsis
sodium_crypto_aead_aes256gcm_keygen(): string
```

Створює випадковий ключ для використання в [sodiumcryptoaeadaes256gcmencrypt()](function.sodium-crypto-aead-aes256gcm-encrypt.html) і [sodiumcryptoaeadaes256gcmdecrypt()](function.sodium-crypto-aead-aes256gcm-decrypt.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає 256-бітний випадковий ключ.