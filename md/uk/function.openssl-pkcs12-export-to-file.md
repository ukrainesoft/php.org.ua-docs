---
navigation:
  - function.openssl-pbkdf2.md: « opensslpbkdf2
  - function.openssl-pkcs12-export.md: opensslpkcs12export »
  - index.md: PHP Manual
  - ref.openssl.md: Функции OpenSSL
title: opensslpkcs12exportтоfile
---
# opensslpkcs12exportтоfile

(PHP 5> = 5.2.2, PHP 7, PHP 8)

opensslpkcs12exportтоfile — Експортує сумісний з PKCS#12 файл сховища сертифікатів

### Опис

```methodsynopsis
openssl_pkcs12_export_to_file(    OpenSSLCertificate|string $certificate,    string $output_filename,    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $private_key,    string $passphrase,    array $options = []): bool
```

**opensslpkcs12exportтоfile()** зберігає `certificate` у файл `output_filename` у форматі PKCS#12.

### Список параметрів

`x509`

Для списку коректних значень дивіться [Параметри ключів/сертифікатів](openssl.certparams.md)

`output_filename`

Шлях до файлу.

`private_key`

Закритий компонент ключа PKCS#12. Допустимі значення дивіться [Параметри закритого/відкритого ключа](openssl.certparams.md)

`passphrase`

Пароль для розблокування PKCS#12.

`options`

Масив опцій. Ключі, які не описані тут, будуть проігноровані.

| Ключ | Описание |
| --- | --- |
| `"extracerts"` | масив додаткових сертифікатів або один сертифікат для включення файлу PKCS#12. |
| `"friendlyname"` | рядок для використання сертифікатом та ключем |

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу `OpenSSL X.509 CSR` |
|  | `private_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу `OpenSSL key` або `OpenSSL X.509` |
