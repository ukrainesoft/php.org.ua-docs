---
navigation:
  - function.openssl-pkey-derive.html: « opensslpkeyderive
  - function.openssl-pkey-export.html: opensslpkeyexport »
  - index.md: PHP Manual
  - ref.openssl.md: Функции OpenSSL
title: opensslpkeyexportтоfile
---
# opensslpkeyexportтоfile

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

opensslpkeyexportтоfile — Записує у файл ключ у форматі PEM

### Опис

```methodsynopsis
openssl_pkey_export_to_file(    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $key,    string $output_filename,    ?string $passphrase = null,    ?array $options = null): bool
```

**opensslpkeyexportтоfile()** записує `key` у форматі PEM у файл `output_filename`

> **Зауваження**: Для коректної роботи цієї функції має бути правильний openssl.cnf. Для більш детальної інформації дивіться зауваження під [разделом установки](openssl.installation.md)

### Список параметрів

`key`

`output_filename`

Шлях до файлу.

`passphrase`

Ключ опціонально захищається паролем `passphrase`

`options`

`options` можна використовувати для тонкого налаштування процесу експорту шляхом вказівки або перевизначення опцій конфігураційного файлу openssl. Дивіться [opensslcsrnew()](function.openssl-csr-new.html) для детальної інформації про `options`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу `OpenSSL key` або `OpenSSL X.509` |
