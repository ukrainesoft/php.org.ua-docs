---
navigation:
  - function.openssl-pkey-export-to-file.md: « opensslpkeyexportтоfile
  - function.openssl-pkey-free.md: opensslpkeyfree »
  - index.md: PHP Manual
  - ref.openssl.md: Функции OpenSSL
title: opensslpkeyexport
---
# opensslpkeyexport

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

opensslpkeyexport — Отримує рядок із ключем у форматі PEM

### Опис

```methodsynopsis
openssl_pkey_export(    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $key,    string &$output,    ?string $passphrase = null,    ?array $options = null): bool
```

**opensslpkeyexport()** експортує `key` у вигляді рядка у форматі PEM і зберігає його в `output` (Передається за посиланням).

> **Зауваження**: Для коректної роботи цієї функції має бути правильний openssl.cnf. Для більш детальної інформації дивіться зауваження під [разделом установки](openssl.installation.md)

### Список параметрів

`key`

`output`

`passphrase`

Ключ опціонально захищається паролем `passphrase`

`options`

`options` можна використовувати для тонкого налаштування процесу експорту шляхом вказівки або перевизначення опцій конфігураційного файлу openssl. Дивіться опис [opensslcsrnew()](function.openssl-csr-new.md) для детальної інформації про `options`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу `OpenSSL key` або `OpenSSL X.509` |
