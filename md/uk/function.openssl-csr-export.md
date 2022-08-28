Експортує CSR у вигляді рядка

-   [« openssl\_csr\_export\_to\_file](function.openssl-csr-export-to-file.html)
    
-   [openssl\_csr\_get\_public\_key »](function.openssl-csr-get-public-key.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Експортує CSR у вигляді рядка
    

# opensslcsrexport

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

opensslcsrexport — Експортує CSR у вигляді рядка

### Опис

```methodsynopsis
openssl_csr_export(OpenSSLCertificateSigningRequest|string $csr, string &$output, bool $no_text = true): bool
```

**opensslcsrexport()** записує запит на підпис сертифіката `csr` у форматі PEM у змінну `output`, яка передається за посиланням.

### Список параметрів

`csr`

Для отримання списку допустимих значень дивіться [параметры CSR](openssl.certparams.html)

`output`

у разі успішного виконання, у цій змінній буде збережено CSR у форматі PEM.

`no_text`

Необов'язковий параметр `notext` впливає на деталізацію повідомлень виводу; якщо він встановлений у **`false`**, то у висновок додається додаткова людиночитана інформація. Значення за замовчуванням `notext` є **`true`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                                                                   |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | `csr` тепер приймає екземпляр [OpenSSLCertificateSigningRequest](class.opensslcertificatesigningrequest.html); раніше приймався ресурс ([resource](language.types.resource.html)) типу `OpenSSL X.509 CSR` |

### Приклади

**Приклад #1 Приклад використання opensslcsrexport()**

```php
<?php
$subject = array(
    "commonName" => "example.com",
);
$private_key = openssl_pkey_new(array(
    "private_key_bits" => 2048,
    "private_key_type" => OPENSSL_KEYTYPE_RSA,
));
$configargs = array(
    'digest_alg' => 'sha256WithRSAEncryption'
);
$csr = openssl_csr_new($subject, $private_key, $configargs);
openssl_csr_export($csr, $csr_string);
echo $csr_string;
?>
```

### Дивіться також

-   [openssl\_csr\_export\_to\_file()](function.openssl-csr-export-to-file.html) - Експортує CSR у файл
-   [openssl\_csr\_new()](function.openssl-csr-new.html) - Генерує CSR
-   [openssl\_csr\_sign()](function.openssl-csr-sign.html) - Підписати CSR за допомогою іншого сертифіката (або ним же) та створити сертифікат