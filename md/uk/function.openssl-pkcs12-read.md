---
navigation:
  - function.openssl-pkcs12-export.md: « openssl\_pkcs12\_export
  - function.openssl-pkcs7-decrypt.md: openssl\_pkcs7\_decrypt »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_pkcs12\_read
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_pkcs12\_read

(PHP 5 >= 5.2.2, PHP 7, PHP 8)

openssl\_pkcs12\_read — Розбирає сховище сертифікатів PKCS#12 у масив

### Опис

```methodsynopsis
openssl_pkcs12_read(string $pkcs12, array &$certificates, string $passphrase): bool
```

\*\*openssl\_pkcs12\_read()\*\*разбирает хранилище сертификатов PKCS#12, заданное в`pkcs12` і поміщає в масив `certificates`

### Список параметрів

`pkcs12`

Вміст сховища сертифікатів, а не його ім'я.

`certificates`

У разі успішного виконання міститиме дані сховища сертифіката (Certificate Store Data).

`passphrase`

Пароль для розшифровки PKCS#12.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** openssl\_pkcs12\_read()\*\*\*\*

```php
<?php
if (!$cert_store = file_get_contents("/certs/file.p12")) {
    echo "Ошибка: невозможно прочитать файл сертификата\n";
    exit;
}

if (openssl_pkcs12_read($cert_store, $cert_info, "my_secret_pass")) {
    echo "Информация об сертификате\n";
    print_r($cert_info);
} else {
    echo "Ошибка: невозможно прочитать хранилище сертификата.\n";
    exit;
}
?>
```
