---
navigation:
  - function.openssl-pkey-derive.md: « openssl\_pkey\_derive
  - function.openssl-pkey-export.md: openssl\_pkey\_export »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_pkey\_export\_to\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_pkey\_export\_to\_file

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

openssl\_pkey\_export\_to\_file — Записує у файл ключ у форматі PEM

### Опис

```methodsynopsis
openssl_pkey_export_to_file(    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $key,    string $output_filename,    ?string $passphrase = null,    ?array $options = null): bool
```

**openssl\_pkey\_export\_to\_file()** записує `key`в формате PEM в файл`output_filename`

> **Зауваження**: Для коректної роботи цієї функції має бути правильний openssl.cnf. Для більш детальної інформації дивіться зауваження під [розділом установки](openssl.installation.md)

### Список параметрів

`key`

`output_filename`

Шлях до файлу.

`passphrase`

Ключ опционально защищается паролем`passphrase`

`options`

`options` можна використовувати для тонкого настроювання процесу експорту шляхом вказівки або перевизначення опцій конфігураційного файлу openssl. Дивіться [openssl\_csr\_new()](function.openssl-csr-new.md) для детальної інформації про `options`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL key`или`OpenSSL X.509` |
