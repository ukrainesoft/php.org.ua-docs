---
navigation:
  - function.openssl-cipher-iv-length.md: « opensslcipherвербlength
  - function.openssl-cms-encrypt.md: opensslcmsencrypt »
  - index.md: PHP Manual
  - ref.openssl.md: Функции OpenSSL
title: opensslcmsdecrypt
---
# opensslcmsdecrypt

(PHP 8)

opensslcmsdecrypt — Розшифровує CMS-повідомлення

### Опис

```methodsynopsis
openssl_cms_decrypt(    string $input_filename,    string $output_filename,    OpenSSLCertificate|string $certificate,    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string|null $private_key = null,    int $encoding = OPENSSL_ENCODING_SMIME): bool
```

Розшифровує CMS-повідомлення.

### Список параметрів

`input_filename`

Ім'я файлу, який містить зашифрований вміст.

`output_filename`

Назва файлу для зберігання розшифрованого вмісту.

`certificate`

Ім'я файлу, який містить сертифікат одержувача.

`private_key`

Назва файлу, що містить ключ PKCS#8.

`encoding`

Кодування вхідного файлу . **`OPENSSL_ENCODING_SMIME`** **`OPENSSL_ENCODING_DER`** або **`OPENSSL_ENCODING_PEM`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
