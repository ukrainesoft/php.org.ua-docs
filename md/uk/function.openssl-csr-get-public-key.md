---
navigation:
  - function.openssl-csr-export.md: « openssl\_csr\_export
  - function.openssl-csr-get-subject.md: openssl\_csr\_get\_subject »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_csr\_get\_public\_key
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_csr\_get\_public\_key

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

openssl\_csr\_get\_public\_key — Повертає відкритий ключ CSR

### Опис

```methodsynopsis
openssl_csr_get_public_key(OpenSSLCertificateSigningRequest|string $csr, bool $short_names = true): OpenSSLAsymmetricKey|false
```

**openssl\_csr\_get\_public\_key()** витягує відкритий ключ з `csr` та готує його для використання в інших функціях.

### Список параметрів

`csr`

Для отримання списку допустимих значень дивіться [параметри CSR](openssl.certparams.md)

`short_names`

**Увага**

Цей параметр ігнорується

### Значення, що повертаються

Повертає [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання повертає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md); раніше повертався ресурс ([resource](language.types.resource.md)) типу`OpenSSL key` |
| 8.0.0 | `csr` тепер приймає екземпляр [OpenSSLCertificateSigningRequest](class.opensslcertificatesigningrequest.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL X.509 CSR` |

### Приклади

**Приклад #1 Приклад використання openssl\_csr\_get\_public\_key()**

```php
<?php
$subject = array(
    "commonName" => "example.com",
);
$private_key = openssl_pkey_new(array(
    "private_key_bits" => 2048,
    "private_key_type" => OPENSSL_KEYTYPE_RSA,
));
$csr = openssl_csr_new($subject, $private_key, array('digest_alg' => 'sha256') );
$public_key = openssl_csr_get_public_key($csr);
$info = openssl_pkey_get_details($public_key);
echo $info['key'];
?>
```

### Дивіться також

-   [openssl\_csr\_get\_subject()](function.openssl-csr-get-subject.md) \- Повертає суб'єкт CSR
-   [openssl\_csr\_new()](function.openssl-csr-new.md) \- Генерує CSR
-   [openssl\_pkey\_get\_details()](function.openssl-pkey-get-details.md) \- Отримує масив з детальною інформацією про ключ
-   [openssl\_pkey\_export\_to\_file()](function.openssl-pkey-export-to-file.md) \- Записує у файл ключ у форматі PEM
-   [openssl\_pkey\_export()](function.openssl-pkey-export.md) \- Отримує рядок із ключем у форматі PEM
