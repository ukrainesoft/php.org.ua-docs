---
navigation:
  - function.openssl-cms-read.md: « openssl\_cms\_read
  - function.openssl-cms-verify.md: openssl\_cms\_verify »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_cms\_sign
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_cms\_sign

(PHP 8)

openssl\_cms\_sign — Підписує файл

### Опис

```methodsynopsis
openssl_cms_sign(    string $input_filename,    string $output_filename,    OpenSSLCertificate|string $certificate,    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $private_key,    ?array $headers,    int $flags = 0,    int $encoding = OPENSSL_ENCODING_SMIME,    ?string $untrusted_certificates_filename = null): bool
```

Підписує файл сертифікатом X.509 та ключем.

### Список параметрів

`input_filename`

Назва файлу для підпису.

`output_filename`

Ім'я файлу для збереження результатів.

`certificate`

Сертификат подписи. Смотрите[параметри ключа/сертифіката](openssl.certparams.md) для отримання списку припустимих значень.

`private_key`

Ключ, пов'язаний з `certificate`Смотрите[параметри ключа/сертифіката](openssl.certparams.md) для отримання списку припустимих значень.

`headers`

Масив заголовків для включення виведення S/MIME.

`flags`

Прапори, що передаються **cms\_sign()**

`encoding`

Кодування вихідного файлу . **`OPENSSL_ENCODING_SMIME`** **`OPENSSL_ENCODING_DER`** або **`OPENSSL_ENCODING_PEM`**

`untrusted_certificates_filename`

Проміжні сертифікати, що включаються до підпису.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** openssl\_cms\_sign()\*\*\*\*

```php
<?php
openssl_cms_sign('input.txt', 'output.txt', 'file://cert.pem', 'file://privkey.pem', null, OPENSSL_CMS_BINARY, OPENSSL_ENCODING_DER, 'chain.pem');
?>
```
