Експортувати файл PKCS7 до масиву сертифікатів PEM

-   [« openssl\_pkcs7\_encrypt](function.openssl-pkcs7-encrypt.html)
    
-   [openssl\_pkcs7\_sign »](function.openssl-pkcs7-sign.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Експортувати файл PKCS7 до масиву сертифікатів PEM
    

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

$file = 'certs.p7b';

$f = file_get_contents($file);
$p7 = array();
$r = openssl_pkcs7_read($f, $p7);

if ($r === false) {
    printf("ОШИБКА: %s не является корректным файлом p7b".PHP_EOL, $file);
        for($e = openssl_error_string(), $i = 0; $e; $e = openssl_error_string(), $i++)
            printf("SSL l%d: %s".PHP_EOL, $i, $e);
    exit(1);
}

print_r($p7);
?>
```

### Дивіться також

-   [openssl\_csr\_sign()](function.openssl-csr-sign.html) - Підписати CSR за допомогою іншого сертифіката (або ним же) та створити сертифікат