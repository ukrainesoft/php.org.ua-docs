Обчислити тег для повідомлення

-   [« sodium\_crypto\_auth\_verify](function.sodium-crypto-auth-verify.html)
    
-   [sodium\_crypto\_box\_keypair\_from\_secretkey\_and\_publickey »](function.sodium-crypto-box-keypair-from-secretkey-and-publickey.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Обчислити тег для повідомлення
    

# sodiumcryptoauth

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoauth — Визначити тег для повідомлення

### Опис

```methodsynopsis
sodium_crypto_auth(string $message, string $key): string
```

Симетрична автентифікація повідомлення за допомогою **sodiumcryptoauth()** забезпечує цілісність, але з конфіденційність.

На відміну від цифрових підписів (наприклад, [sodium\_crypto\_sign\_detached()](function.sodium-crypto-sign-detached.html)), будь-яка сторона, здатна перевірити повідомлення, також здатна перевірити справжність своїх власних повідомлень. (Отже, симетрична автентифікація.)

### Список параметрів

`message`

Повідомлення, яке ви маєте намір підтвердити.

`key`

Ключ аутентифікації

### Значення, що повертаються

Тег аутентифікації