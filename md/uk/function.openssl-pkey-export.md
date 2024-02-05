---
navigation:
  - function.openssl-pkey-export-to-file.md: « openssl\_pkey\_export\_to\_file
  - function.openssl-pkey-free.md: openssl\_pkey\_free »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_pkey\_export
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_pkey\_export

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

openssl\_pkey\_export — Отримує рядок із ключем у форматі PEM

### Опис

```methodsynopsis
openssl_pkey_export(    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $key,    string &$output,    ?string $passphrase = null,    ?array $options = null): bool
```

**openssl\_pkey\_export()** експортує `key` у вигляді рядка у форматі PEM і зберігає його в `output` (Передається за посиланням).

> **Зауваження**: Для коректної роботи цієї функції має бути правильний openssl.cnf. Для більш детальної інформації дивіться зауваження під [розділом установки](openssl.installation.md)

### Список параметрів

`key`

`output`

`passphrase`

Ключ опционально защищается паролем`passphrase`

`options`

`options` можна використовувати для тонкого настроювання процесу експорту шляхом вказівки або перевизначення опцій конфігураційного файлу openssl. Дивіться опис [openssl\_csr\_new()](function.openssl-csr-new.md) для детальної інформації про `options`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL key`или`OpenSSL X.509` |
