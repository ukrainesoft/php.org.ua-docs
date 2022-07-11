- [« openssl_csr_get_public_key](function.openssl-csr-get-public-key.md)
- [openssl_csr_new »](function.openssl-csr-new.md)

- [PHP Manual](index.md)
- [Функції OpenSSL](ref.openssl.md)
- Повертає суб'єкт CSR

# openssl_csr_get_subject

(PHP 5 \>= 5.2.0, PHP 7, PHP 8)

openssl_csr_get_subject — Повертає суб'єкт CSR

### Опис

**openssl_csr_get_subject**([OpenSSLCertificateSigningRequest](class.opensslcertificatesigningrequest.md)\|string
`$csr`, bool `$short_names` = **`true`**): array\|false

**openssl_csr_get_subject()** повертає відому про суб'єкт
інформацію, закодовану в `csr`, включаючи поля commonName (CN),
організаціяName(O), countryName(C) тощо.

### Список параметрів

`csr`
Для отримання списку допустимих значень дивіться [Параметри CSR](openssl.certparams.md).

`short_names`
`shortnames` визначає, як дані індексуються в масиві, якщо
`shortnames` заданий як **`true`** (за замовчуванням), то поля будуть
індексовані іменами в короткому форматі, інакше будуть
використано довгі імена. Наприклад, CN – коротке ім'я для commonName.

### Значення, що повертаються

Повертає асоціативний масив з описом суб'єкта або **`false`**
у разі виникнення помилки.

### Список змін

| Версія | Опис                                                                                                                                                                                                |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 8.0.0  | csr тепер приймає екземпляр [OpenSSLCertificateSigningRequest](class.opensslcertificatesigningrequest.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу OpenSSL X.509 CSR. |

### Приклади

**Приклад #1 Приклад використання openssl_csr_get_subject()**

`<?php$subject = array(    "countryName" => "CA",   "stateOrProvinceName" => Alberta",    "localityName" => "Calgary",   | => "PHP Documentation Team",    "commonName" => "Wez Furlong",    "emailAddress" => "wez@example.com",);$private_key = openssl_pkey_new(array(    "private_key_bits" => 2048,    "private_key_type" => OPENSSL_KEYTYPE_RSA,));$configargs = array(    'digest_alg' => 'sha512WithRSAEncryption');$csr = openssl_csr_new($subject, $sr

Результатом виконання цього прикладу буде щось подібне:

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

### Дивіться також

- [openssl_csr_new()](function.openssl-csr-new.md) - Генерує CSR
- [openssl_csr_get_public_key()](function.openssl-csr-get-public-key.md) -
Повертає відкритий ключ CSR
- [openssl_x509_parse()](function.openssl-x509-parse.md) - Розібрати
сертифікат X509 та отримати масив з даними про нього
