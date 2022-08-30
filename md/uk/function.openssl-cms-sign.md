Підписує файл

-   [« opensslcmsread](function.openssl-cms-read.html)
    
-   [opensslcmsverify »](function.openssl-cms-verify.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Підписує файл
    

# opensslcmssign

(PHP 8)

opensslcmssign — Підписує файл

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

Сертифікат підпису. Дивіться [параметры ключа/сертификата](openssl.certparams.html) для отримання списку припустимих значень.

`private_key`

Ключ, пов'язаний з `certificate`. Дивіться [параметры ключа/сертификата](openssl.certparams.html) для отримання списку припустимих значень.

`headers`

Масив заголовків для включення виведення S/MIME.

`flags`

Прапори, що передаються **cmssign()**

`encoding`

Кодування вихідного файлу . **`OPENSSL_ENCODING_SMIME`** **`OPENSSL_ENCODING_DER`** або **`OPENSSL_ENCODING_PEM`**

`untrusted_certificates_filename`

Проміжні сертифікати, що включаються до підпису.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **opensslcmssign()****

```php
<?php
openssl_cms_sign('input.txt', 'output.txt', 'file://cert.pem', 'file://privkey.pem', null, OPENSSL_CMS_BINARY, OPENSSL_ENCODING_DER, 'chain.pem');
?>
```