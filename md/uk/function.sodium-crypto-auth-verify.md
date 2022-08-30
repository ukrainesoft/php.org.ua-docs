Перевіряє, чи допустимо тег для повідомлення

-   [« sodiumcryptoauthkeygen](function.sodium-crypto-auth-keygen.html)
    
-   [sodiumcryptoauth »](function.sodium-crypto-auth.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Перевіряє, чи допустимо тег для повідомлення
    

# sodiumcryptoauthverify

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoauthverify — Перевіряє, чи допустимо тег для повідомлення

### Опис

```methodsynopsis
sodium_crypto_auth_verify(string $mac, string $message, string $key): bool
```

Перевіряє, що тег автентифікації дійсний для цього повідомлення та ключа.

На відміну від цифрових підписів (наприклад, [sodiumcryptosignverifydetached()](function.sodium-crypto-sign-verify-detached.html)), будь-яка сторона, здатна перевірити повідомлення, також здатна перевірити справжність своїх повідомлень. (Отже, симетрична автентифікація.)

### Список параметрів

`mac`

Тег аутентифікації, створений [sodiumcryptoauth()](function.sodium-crypto-auth.html)

`message`

Повідомлення

`key`

Ключ аутентифікації

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.