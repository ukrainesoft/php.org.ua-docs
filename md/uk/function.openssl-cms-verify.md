---
navigation:
  - function.openssl-cms-sign.md: « openssl\_cms\_sign
  - function.openssl-csr-export-to-file.md: openssl\_csr\_export\_to\_file »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_cms\_verify
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_cms\_verify

(PHP 8)

openssl\_cms\_verify — Перевіряє підпис CMS

### Опис

```methodsynopsis
openssl_cms_verify(    string $input_filename,    int $flags = 0,    ?string $certificates = null,    array $ca_info = [],    ?string $untrusted_certificates_filename = null,    ?string $content = null,    ?string $pk7 = null,    ?string $sigfile = null,    int $encoding = OPENSSL_ENCODING_SMIME): bool
```

Перевіряє підпис CMS, прикріплений або від'єднаний, із зазначеним кодуванням.

### Список параметрів

`input_filename`

Вхідний файл

`flags`

Прапори, що передаються **cms\_verify()**

`certificates`

Файл із сертифікатом, який підписав і, на вибір, проміжними сертифікатами.

`ca_info`

Масив, що містить самозавірені сертифікати центру сертифікації.

`untrusted_certificates_filename`

Файл, який містить додаткові проміжні сертифікати.

`content`

Файл, який вказує на вміст, коли підписи від'єднані.

`pk7`

`sigfile`

Файл, який потрібно зберегти підпис.

`encoding`

Кодування вхідного файлу . **`OPENSSL_ENCODING_SMIME`** **`OPENSSL_ENCODING_DER`** або **`OPENSSL_ENCODING_PEM`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
