Підписати повідомлення

-   [« sodiumcryptoshorthash](function.sodium-crypto-shorthash.html)
    
-   [sodiumcryptosigned25519пктоcurve25519 »](function.sodium-crypto-sign-ed25519-pk-to-curve25519.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Підписати повідомлення
    

# sodiumcryptosigndetached

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptosigndetached — Підписати повідомлення

### Опис

```methodsynopsis
sodium_crypto_sign_detached(string $message, string $secret_key): string
```

Підписує повідомлення секретним ключем, який можна перевірити за допомогою відкритого ключа. Функція повертає від'єднаний підпис.

### Список параметрів

`message`

Повідомлення для підписання.

`secret_key`

Секретний ключ. Дивіться [sodiumcryptosignsecretkey()](function.sodium-crypto-sign-secretkey.html)

### Значення, що повертаються

Криптографічний підпис.