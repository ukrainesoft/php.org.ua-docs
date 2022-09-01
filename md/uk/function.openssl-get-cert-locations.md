---
navigation:
  - function.openssl-free-key.html: « opensslfreekey
  - function.openssl-get-cipher-methods.html: opensslgetciphermethods »
  - index.md: PHP Manual
  - ref.openssl.md: Функции OpenSSL
title: opensslgetcertlocations
---
# opensslgetcertlocations

(PHP 5> = 5.6.0, PHP 7, PHP 8)

opensslgetcertlocations — Отримати доступні місця розташування сертифікатів

### Опис

```methodsynopsis
openssl_get_cert_locations(): array
```

**opensslgetcertlocations()** повертає масив з інформацією про доступні сховища, в яких відбуватиметься пошук SSL сертифікатів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив із місцезнаходженням сховищ сертифікатів.

### Приклади

**Приклад #1 Приклад використання **opensslgetcertlocations()****

```php
<?php
var_dump(openssl_get_cert_locations());
?>
```

Результат виконання цього прикладу:

```
array(8) {
  ["default_cert_file"]=>
  string(21) "/usr/lib/ssl/cert.pem"
  ["default_cert_file_env"]=>
  string(13) "SSL_CERT_FILE"
  ["default_cert_dir"]=>
  string(18) "/usr/lib/ssl/certs"
  ["default_cert_dir_env"]=>
  string(12) "SSL_CERT_DIR"
  ["default_private_dir"]=>
  string(20) "/usr/lib/ssl/private"
  ["default_default_cert_area"]=>
  string(12) "/usr/lib/ssl"
  ["ini_cafile"]=>
  string(0) ""
  ["ini_capath"]=>
  string(0) ""
}
```
