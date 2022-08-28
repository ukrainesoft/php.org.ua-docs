Перевірити підпис для повідомлення

-   [« sodium\_crypto\_sign\_seed\_keypair](function.sodium-crypto-sign-seed-keypair.html)
    
-   [sodium\_crypto\_sign »](function.sodium-crypto-sign.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Перевірити підпис для повідомлення
    

# sodiumcryptosignverifydetached

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptosignverifydetached — Перевірити підпис для повідомлення

### Опис

```methodsynopsis
sodium_crypto_sign_verify_detached(string $signature, string $message, string $public_key): bool
```

Перевіряє підпис для повідомлення

### Список параметрів

`signature`

Криптографічний підпис, отриманий за допомогою [sodium\_crypto\_sign\_detached()](function.sodium-crypto-sign-detached.html)

`message`

Перевірене повідомлення

`public_key`

Відкритий ключ ed25519

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.