Перевірити, що підписане повідомлення має коректний підпис

-   [« sodium\_crypto\_sign\_keypair](function.sodium-crypto-sign-keypair.html)
    
-   [sodium\_crypto\_sign\_publickey\_from\_secretkey »](function.sodium-crypto-sign-publickey-from-secretkey.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Перевірити, що підписане повідомлення має коректний підпис
    

# sodiumcryptosignopen

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptosignopen — Перевірити, чи підписане повідомлення має коректний підпис

### Опис

```methodsynopsis
sodium_crypto_sign_open(string $signed_message, string $public_key): string|false
```

Перевіряє підпис, прикріплений до повідомлення, та повертає повідомлення

### Список параметрів

`signed_message`

Повідомлення, підписане [sodium\_crypto\_sign()](function.sodium-crypto-sign.html)

`public_key`

Відкритий ключ Ed25519

### Значення, що повертаються

У разі успішного виконання повертає вихідне підписане повідомлення або **`false`** у разі виникнення помилки.