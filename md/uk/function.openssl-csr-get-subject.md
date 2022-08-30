Повертає суб'єкт CSR

-   [« opensslcsrgetpublickey](function.openssl-csr-get-public-key.html)
    
-   [opensslcsrnew »](function.openssl-csr-new.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Повертає суб'єкт CSR
    

# opensslcsrgetsubject

(PHP 5> = 5.2.0, PHP 7, PHP 8)

opensslcsrgetsubject — Повертає суб'єкт CSR

### Опис

```methodsynopsis
openssl_csr_get_subject(OpenSSLCertificateSigningRequest|string $csr, bool $short_names = true): array|false
```

**opensslcsrgetsubject()** повертає відому про суб'єкт інформацію закодовану в `csr`, включаючи поля commonName (CN), organizationName (O), countryName (C) і т.д.

### Список параметрів

`csr`

Для отримання списку допустимих значень дивіться [параметри CSR](openssl.certparams.html)

`short_names`

`shortnames` визначає, як дані індексуються в масиві, якщо `shortnames` заданий як **`true`** (за замовчуванням), поля будуть індексовані іменами в короткому форматі, в іншому випадку будуть використані довгі імена. Наприклад, CN – коротке ім'я для commonName.

### Значення, що повертаються

Повертає асоціативний масив з описом суб'єкта або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `csr` тепер приймає екземпляр [OpenSSLCertificateSigningRequest](class.opensslcertificatesigningrequest.html); раніше приймався ресурс ([resource](language.types.resource.html)) типу `OpenSSL X.509 CSR` |

### Приклади

**Приклад #1 Приклад використання opensslcsrgetsubject()**

```php
<?php
$subject = array(
    "countryName" => "CA",
    "stateOrProvinceName" => "Alberta",
    "localityName" => "Calgary",
    "organizationName" => "XYZ Widgets Inc",
    "organizationalUnitName" => "PHP Documentation Team",
    "commonName" => "Wez Furlong",
    "emailAddress" => "wez@example.com",
);
$private_key = openssl_pkey_new(array(
    "private_key_bits" => 2048,
    "private_key_type" => OPENSSL_KEYTYPE_RSA,
));
$configargs = array(
    'digest_alg' => 'sha512WithRSAEncryption'
);
$csr = openssl_csr_new($subject, $privkey, $configargs);
print_r(openssl_csr_get_subject($csr));
?>
```

Результатом виконання цього прикладу буде щось подібне:

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

-   [opensslcsrnew()](function.openssl-csr-new.html) - Генерує CSR
-   [opensslcsrgetpublickey()](function.openssl-csr-get-public-key.html) - Повертає відкритий ключ CSR
-   [opensslx509parse()](function.openssl-x509-parse.html) - Розібрати сертифікат X509 та отримати масив з даними про нього