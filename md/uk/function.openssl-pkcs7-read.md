---
navigation:
  - function.openssl-pkcs7-encrypt.md: « openssl\_pkcs7\_encrypt
  - function.openssl-pkcs7-sign.md: openssl\_pkcs7\_sign »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_pkcs7\_read
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_pkcs7\_read

(PHP 7 >= 7.2.0, PHP 8)

openssl\_pkcs7\_read — Експортувати файл PKCS7 до масиву сертифікатів PEM

### Опис

```methodsynopsis
openssl_pkcs7_read(string $data, array &$certificates): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`data`

Рядок даних, які потрібно проаналізувати (формат p7b).

`certificates`

Масив сертифікатів PEM із вхідних даних p7b.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Отримання масиву PEM із файлу P7B**

```php
<?php

$file = 'certs.p7b';

$f = file_get_contents($file);
$p7 = array();
$r = openssl_pkcs7_read($f, $p7);

if ($r === false) {
    printf("ОШИБКА: %s не является корректным файлом p7b".PHP_EOL, $file);
        for($e = openssl_error_string(), $i = 0; $e; $e = openssl_error_string(), $i++)
            printf("SSL l%d: %s".PHP_EOL, $i, $e);
    exit(1);
}

print_r($p7);
?>
```

### Дивіться також

-   [openssl\_csr\_sign()](function.openssl-csr-sign.md) \- Підписати CSR за допомогою іншого сертифіката (або ним же) та створити сертифікат
