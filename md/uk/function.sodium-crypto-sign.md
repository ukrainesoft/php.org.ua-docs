Підписати повідомлення

-   [« sodium\_crypto\_sign\_verify\_detached](function.sodium-crypto-sign-verify-detached.html)
    
-   [sodium\_crypto\_stream\_keygen »](function.sodium-crypto-stream-keygen.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Підписати повідомлення
    

# sodiumcryptosign

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptosign — Підписати повідомлення

### Опис

```methodsynopsis
sodium_crypto_sign(string $message, string $secret_key): string
```

Підписує повідомлення секретним ключем, який можна перевірити за допомогою відкритого ключа. Функція підписує повідомлення. Подробиці у розділі [sodium\_crypto\_sign\_detached()](function.sodium-crypto-sign-detached.html) для окремих підписів.

### Список параметрів

`message`

Повідомлення для підпису.

`secret_key`

Секретний ключ. Дивіться [sodium\_crypto\_sign\_secretkey()](function.sodium-crypto-sign-secretkey.html)

### Значення, що повертаються

Підписане повідомлення (не зашифроване).