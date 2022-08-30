Перевіряє, що пароль відповідає хешу

-   [« sodiumcryptopwhashstrneedsrehash](function.sodium-crypto-pwhash-str-needs-rehash.html)
    
-   [sodiumcryptopwhashstr »](function.sodium-crypto-pwhash-str.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Sodium](ref.sodium.html)
    
-   Перевіряє, що пароль відповідає хешу
    

# sodiumcryptopwhashstrverify

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptopwhashstrverify — Перевіряє, чи пароль відповідає хешу

### Опис

```methodsynopsis
sodium_crypto_pwhash_str_verify(string $hash, string $password): bool
```

Перевіряє, що хеш пароля, створений [sodiumcryptopwhashstr()](function.sodium-crypto-pwhash-str.html)відповідає заданому паролю. Зверніть увагу, що в цій функції порядок аргументів не відповідає порядку аргументів у схожій функції [passwordverify()](function.password-verify.html)

### Список параметрів

`hash`

Хеш, створений функцією [passwordhash()](function.password-hash.html)

`password`

Користувальницький пароль.

### Значення, що повертаються

Повертає **`true`**, якщо пароль відповідає хешу, та **`false`**, якщо ні.

### Примітки

> **Зауваження**
> 
> Хеші обчислюються за допомогою алгоритму Argon2ID, який добре протистоїть обом видам атак: GPU і атакам по сторонньому каналу.

### Дивіться також

-   [sodiumcryptopwhashstr()](function.sodium-crypto-pwhash-str.html) - Отримати ASCII-кодований хеш
-   [passwordhash()](function.password-hash.html) - Створює хеш пароля
-   [passwordverify()](function.password-verify.html) - Перевіряє, чи пароль хешу відповідає