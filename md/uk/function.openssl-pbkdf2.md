Генерує рядки PKCS5 v2 PBKDF2

-   [« opensslopen](function.openssl-open.html)
    
-   [opensslpkcs12exportтоfile »](function.openssl-pkcs12-export-to-file.html)
    
-   [PHP Manual](index.md)
    
-   [Функции OpenSSL](ref.openssl.md)
    
-   Генерує рядки PKCS5 v2 PBKDF2
    

# opensslpbkdf2

(PHP 5> = 5.5.0, PHP 7, PHP 8)

opensslpbkdf2 — Генерує рядки PKCS5 v2 PBKDF2

### Опис

```methodsynopsis
openssl_pbkdf2(    string $password,    string $salt,    int $key_length,    int $iterations,    string $digest_algo = "sha1"): string|false
```

**opensslpbkdf2()** обчислює PBKDF2 (Password-Based Key Derivation Function 2), функцію деривації ключа, визначену в PKCS5 v2.

### Список параметрів

`password`

Пароль, з якого буде згенеровано ключ.

`salt`

PBKDF2 рекомендує використовувати криптографічну сіль як мінімум 64 біти (8 байт) завдовжки.

`key_length`

Довжина генерованого ключа.

`iterations`

Кількість ітерацій . [» NIST рекомендует как минимум 10,000](https://pages.nist.gov/800-63-3/sp800-63b.html#sec5)

`digest_algo`

Опціональний алгоритм хешування отриманий з [opensslgetмдmethods()](function.openssl-get-md-methods.html). Типово SHA-1.

### Значення, що повертаються

Повертає необроблений бінарний рядок або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання opensslpbkdf2()**

```php
<?php
$password = 'yOuR-pAs5w0rd-hERe';
$salt = openssl_random_pseudo_bytes(12);
$keyLength = 40;
$iterations = 10000;
$generated_key = openssl_pbkdf2($password, $salt, $keyLength, $iterations, 'sha256');
echo bin2hex($generated_key)."\n";
echo base64_encode($generated_key)."\n";
?>
```

### Дивіться також

-   [hashpbkdf2()](function.hash-pbkdf2.html) - Формування ключа PBKDF2 для заданих вхідних даних
-   [opensslgetмдmethods()](function.openssl-get-md-methods.html) - Отримати список доступних методів хешування