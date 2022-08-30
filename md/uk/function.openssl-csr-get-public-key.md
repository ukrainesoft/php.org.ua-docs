Повертає відкритий ключ CSR

-   [« opensslcsrexport](function.openssl-csr-export.html)
    
-   [opensslcsrgetsubject »](function.openssl-csr-get-subject.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Повертає відкритий ключ CSR
    

# opensslcsrgetpublickey

(PHP 5> = 5.2.0, PHP 7, PHP 8)

opensslcsrgetpublickey — Повертає відкритий ключ CSR

### Опис

```methodsynopsis
openssl_csr_get_public_key(OpenSSLCertificateSigningRequest|string $csr, bool $short_names = true): OpenSSLAsymmetricKey|false
```

**opensslcsrgetpublickey()** витягує відкритий ключ з `csr` та готує його для використання в інших функціях.

### Список параметрів

`csr`

Для отримання списку допустимих значень дивіться [параметры CSR](openssl.certparams.html)

`short_names`

**Увага**

Цей параметр ігнорується

### Значення, що повертаються

Повертає [OpenSSLAsymmetricKey](class.opensslasymmetrickey.html) у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                                                                   |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | У разі успішного виконання повертає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.html); раніше повертався ресурс ([resource](language.types.resource.html)) типу `OpenSSL key`              |
|        | `csr` тепер приймає екземпляр [OpenSSLCertificateSigningRequest](class.opensslcertificatesigningrequest.html); раніше приймався ресурс ([resource](language.types.resource.html)) типу `OpenSSL X.509 CSR` |

### Приклади

**Приклад #1 Приклад використання opensslcsrgetpublickey()**

```php
<?php
$subject = array(
    "commonName" => "example.com",
);
$private_key = openssl_pkey_new(array(
    "private_key_bits" => 2048,
    "private_key_type" => OPENSSL_KEYTYPE_RSA,
));
$csr = openssl_csr_new($subject, $private_key, array('digest_alg' => 'sha256') );
$public_key = openssl_csr_get_public_key($csr);
$info = openssl_pkey_get_details($public_key);
echo $info['key'];
?>
```

### Дивіться також

-   [opensslcsrgetsubject()](function.openssl-csr-get-subject.html) - Повертає суб'єкт CSR
-   [opensslcsrnew()](function.openssl-csr-new.html) - Генерує CSR
-   [opensslpkeygetdetails()](function.openssl-pkey-get-details.html) - Отримує масив з детальною інформацією про ключ
-   [opensslpkeyexportтоfile()](function.openssl-pkey-export-to-file.html) - Записує у файл ключ у форматі PEM
-   [opensslpkeyexport()](function.openssl-pkey-export.html) - Отримує рядок із ключем у форматі PEM