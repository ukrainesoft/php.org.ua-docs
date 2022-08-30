Перевірити, чи підтримує обладнання AES256-GCM

-   [« sodiumcryptoaeadaes256gcmencrypt](function.sodium-crypto-aead-aes256gcm-encrypt.html)
    
-   [sodiumcryptoaeadaes256gcmkeygen »](function.sodium-crypto-aead-aes256gcm-keygen.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Перевірити, чи підтримує обладнання AES256-GCM
    

# sodiumcryptoaeadaes256gcmісavailable

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoaeadaes256gcmісavailable — Перевірити, чи підтримує обладнання AES256-GCM

### Опис

```methodsynopsis
sodium_crypto_aead_aes256gcm_is_available(): bool
```

Значення цієї функції залежить від того, чи апаратне прискорення AES підтримує обладнання.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо шифрування за допомогою AES-256-GCM безпечне, інакше повертає **`false`**