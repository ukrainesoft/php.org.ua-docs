---
navigation:
  - function.openssl-pkcs12-export-to-file.md: « openssl\_pkcs12\_export\_to\_file
  - function.openssl-pkcs12-read.md: openssl\_pkcs12\_read »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_pkcs12\_export
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_pkcs12\_export

(PHP 5 >= 5.2.2, PHP 7, PHP 8)

openssl\_pkcs12\_export — Експортує сумісний із PKCS#12 файл сховища сертифікатів у змінну

### Опис

```methodsynopsis
openssl_pkcs12_export(    OpenSSLCertificate|string $certificate,    string &$output,    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $private_key,    string $passphrase,    array $options = []): bool
```

**openssl\_pkcs12\_export()** зберігає `x509`в переменную`out`в формате PKCS#12.

### Список параметрів

`x509`

Для списку коректних значень дивіться [Параметри ключів/сертифікатів](openssl.certparams.md)

`output`

У разі успішного виконання міститиме PKCS#12.

`private_key`

Компонент закритого ключа PKCS#12. Список допустимих значень дивіться на сторінці [параметрів відкритого/закритого ключа](openssl.certparams.md)

`passphrase`

Пароль для шифрування PKCS#12.

`options`

Масив опцій. Ключі, які не описані тут, будуть проігноровані.

| Ключ | Опис |
| --- | --- |
| `"extracerts"` | масив додаткових сертифікатів або один сертифікат для включення файлу PKCS#12. |
| `"friendly_name"` | рядок для використання сертифікатом та ключем |

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL X.509 CSR` |
| 8.0.0 | `private_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL key`или`OpenSSL X.509` |
