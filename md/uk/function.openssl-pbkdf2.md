---
navigation:
  - function.openssl-open.md: « openssl\_open
  - function.openssl-pkcs12-export-to-file.md: openssl\_pkcs12\_export\_to\_file »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_pbkdf2
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_pbkdf2

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

openssl\_pbkdf2 — Генерує рядки PKCS5 v2 PBKDF2

### Опис

```methodsynopsis
openssl_pbkdf2(    string $password,    string $salt,    int $key_length,    int $iterations,    string $digest_algo = "sha1"): string|false
```

**openssl\_pbkdf2()** обчислює PBKDF2 (Password-Based Key Derivation Function 2), функцію деривації ключа, визначену в PKCS5 v2.

### Список параметрів

`password`

Пароль, з якого буде згенеровано ключ.

`salt`

PBKDF2 рекомендує використовувати криптографічну сіль як мінімум 64 біти (8 байт) завдовжки.

`key_length`

Довжина генерованого ключа.

`iterations`

Кількість ітерацій . [» NIST рекомендує як мінімум 10,000](https://pages.nist.gov/800-63-3/sp800-63b.md#sec5)

`digest_algo`

Опціональний алгоритм хешування отриманий з [openssl\_get\_md\_methods()](function.openssl-get-md-methods.md)По умолчанию SHA-1.

### Значення, що повертаються

Повертає необроблений бінарний рядок або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання openssl\_pbkdf2()**

```php
<?php
$password = 'password';
$salt = openssl_random_pseudo_bytes(16);
$keyLength = 20;
$iterations = 600000;
$generated_key = openssl_pbkdf2($password, $salt, $keyLength, $iterations, 'sha256');
echo bin2hex($generated_key)."\n";
echo base64_encode($generated_key)."\n";
?>
```

### Дивіться також

-   [hash\_pbkdf2()](function.hash-pbkdf2.md) \- Формування ключа PBKDF2 для заданих вхідних даних
-   [openssl\_get\_md\_methods()](function.openssl-get-md-methods.md) \- Отримати список доступних методів хешування
