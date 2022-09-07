---
navigation:
  - function.openssl-pkcs7-encrypt.md: « opensslpkcs7encrypt
  - function.openssl-pkcs7-sign.md: opensslpkcs7sign »
  - index.md: PHP Manual
  - ref.openssl.md: Функции OpenSSL
title: opensslpkcs7read
---
# opensslpkcs7read

(PHP 7> = 7.2.0, PHP 8)

opensslpkcs7read — Експортувати файл PKCS7 до масиву сертифікатів PEM

### Опис

```methodsynopsis
openssl_pkcs7_read(string $data, array &$certificates): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`data`

Рядок даних, які потрібно проаналізувати (формат p7b).

`certificates`

Масив сертифікатів PEM із вхідних даних p7b.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Get a PEM array from a P7B file**

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

-   [opensslcsrsign()](function.openssl-csr-sign.md) - Підписати CSR за допомогою іншого сертифіката (або ним же) та створити сертифікат
