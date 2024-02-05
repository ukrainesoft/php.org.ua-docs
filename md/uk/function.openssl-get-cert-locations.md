---
navigation:
  - function.openssl-free-key.md: « openssl\_free\_key
  - function.openssl-get-cipher-methods.md: openssl\_get\_cipher\_methods »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_get\_cert\_locations
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_get\_cert\_locations

(PHP 5 >= 5.6.0, PHP 7, PHP 8)

openssl\_get\_cert\_locations — Отримати доступні місця розташування сертифікатів

### Опис

```methodsynopsis
openssl_get_cert_locations(): array
```

**openssl\_get\_cert\_locations()** повертає масив з інформацією про доступні сховища, в яких відбуватиметься пошук SSL сертифікатів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив із місцезнаходженням сховищ сертифікатів.

### Приклади

**Пример #1 Пример использования**openssl\_get\_cert\_locations()\*\*\*\*

```php
<?php
var_dump(openssl_get_cert_locations());
?>
```

Результат виконання наведеного прикладу:

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
