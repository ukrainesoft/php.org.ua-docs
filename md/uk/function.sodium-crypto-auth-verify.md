Перевіряє, чи допустимо тег для повідомлення

-   [« sodium\_crypto\_auth\_keygen](function.sodium-crypto-auth-keygen.html)
    
-   [sodium\_crypto\_auth »](function.sodium-crypto-auth.html)
    
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

На відміну від цифрових підписів (наприклад, [sodium\_crypto\_sign\_verify\_detached()](function.sodium-crypto-sign-verify-detached.html)), будь-яка сторона, здатна перевірити повідомлення, також здатна перевірити справжність своїх повідомлень. (Отже, симетрична автентифікація.)

### Список параметрів

`mac`

Тег аутентифікації, створений [sodium\_crypto\_auth()](function.sodium-crypto-auth.html)

`message`

Повідомлення

`key`

Ключ аутентифікації

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.