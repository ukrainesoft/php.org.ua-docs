---
navigation:
  - function.openssl-verify.md: « opensslverify
  - function.openssl-x509-checkpurpose.md: opensslx509checkpurpose »
  - index.md: PHP Manual
  - ref.openssl.md: Функции OpenSSL
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
|  | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу `OpenSSL X.509` |
|  | `private_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу `OpenSSL key` або `OpenSSL X.509` |
