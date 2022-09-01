---
navigation:
  - function.openssl-verify.html: « opensslverify
  - function.openssl-x509-checkpurpose.html: opensslx509checkpurpose »
  - index.html: PHP Manual
  - ref.openssl.html: Функции OpenSSL
title: opensslx509checkprivatekey
---
# opensslx509checkprivatekey

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

opensslx509checkprivatekey — Перевірити, чи секретний ключ відноситься до сертифіката

### Опис

```methodsynopsis
openssl_x509_check_private_key(OpenSSLCertificate|string $certificate, OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $private_key): bool
```

Перевіряє, що заданий `private_key` є секретним ключем, що відповідає сертифікату `certificate`

**Увага**

Функція не перевіряє, чи є `private_key` секретним ключем чи ні. Він просто порівнює відкриті дані (наприклад, експоненту та модуль ключа RSA) та/або параметри ключа (наприклад, параметри EC для EC-ключа) пари ключів.

Тобто, якщо помістити в `private_key` відповідний відкритий ключ, то функція може повернути **`true`**

### Список параметрів

`certificate`

Сертифікат

`private_key`

Ключ.

### Значення, що повертаються

Повертає **`true`**, якщо `private_key` є ключем відповідним сертифікату `certificate`, або **`false`** в іншому випадку.

### список змін

| Версия | Описание |
| --- | --- |
|  | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.html); раніше приймався ресурс ([resource](language.types.resource.html)) типу `OpenSSL X.509` |
|  | `private_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.html) або [OpenSSLCertificate](class.opensslcertificate.html); раніше приймався ресурс ([resource](language.types.resource.html)) типу `OpenSSL key` або `OpenSSL X.509` |
