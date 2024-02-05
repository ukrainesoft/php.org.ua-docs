---
navigation:
  - function.openssl-csr-get-public-key.md: « openssl\_csr\_get\_public\_key
  - function.openssl-csr-new.md: openssl\_csr\_new »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_csr\_get\_subject
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_csr\_get\_subject

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

openssl\_csr\_get\_subject — Повертає суб'єкт CSR

### Опис

```methodsynopsis
openssl_csr_get_subject(OpenSSLCertificateSigningRequest|string $csr, bool $short_names = true): array|false
```

**openssl\_csr\_get\_subject()** повертає відому про суб'єкт інформацію закодовану в `csr`, включаючи поля commonName (CN), organizationName (O), countryName (C) і т.д.

### Список параметрів

`csr`

Для отримання списку допустимих значень дивіться [параметри CSR](openssl.certparams.md)

`short_names`

`shortnames` визначає, як дані індексуються в масиві, якщо `shortnames`задан как\*\*`true`\*\* (за замовчуванням), поля будуть індексовані іменами в короткому форматі, в іншому випадку будуть використані довгі імена. Наприклад, CN – коротке ім'я для commonName.

### Значення, що повертаються

Повертає асоціативний масив з описом суб'єкта або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `csr` тепер приймає екземпляр [OpenSSLCertificateSigningRequest](class.opensslcertificatesigningrequest.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL X.509 CSR` |

### Приклади

**Приклад #1 Приклад використання openssl\_csr\_get\_subject()**

```php
<?php
$subject = array(
    "countryName" => "CA",
    "stateOrProvinceName" => "Alberta",
    "localityName" => "Calgary",
    "organizationName" => "XYZ Widgets Inc",
    "organizationalUnitName" => "PHP Documentation Team",
    "commonName" => "Wez Furlong",
    "emailAddress" => "wez@example.com",
);
$private_key = openssl_pkey_new(array(
    "private_key_bits" => 2048,
    "private_key_type" => OPENSSL_KEYTYPE_RSA,
));
$configargs = array(
    'digest_alg' => 'sha512WithRSAEncryption'
);
$csr = openssl_csr_new($subject, $privkey, $configargs);
print_r(openssl_csr_get_subject($csr));
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [C] => CA
    [ST] => Alberta
    [L] => Calgary
    [O] => XYZ Widgets Inc
    [OU] => PHP Documentation Team
    [CN] => Wez Furlong
    [emailAddress] => wez@example.com
)
```

### Дивіться також

-   [openssl\_csr\_new()](function.openssl-csr-new.md) \- Генерує CSR
-   [openssl\_csr\_get\_public\_key()](function.openssl-csr-get-public-key.md) \- Повертає відкритий ключ CSR
-   [openssl\_x509\_parse()](function.openssl-x509-parse.md) \- Розібрати сертифікат X509 та отримати масив з даними про нього
