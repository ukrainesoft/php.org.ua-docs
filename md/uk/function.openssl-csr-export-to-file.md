---
navigation:
  - function.openssl-cms-verify.html: « opensslcmsverify
  - function.openssl-csr-export.html: opensslcsrexport »
  - index.md: PHP Manual
  - ref.openssl.md: Функции OpenSSL
title: opensslcsrexportтоfile
---
# opensslcsrexportтоfile

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

opensslcsrexportтоfile — Експортує CSR у файл

### Опис

```methodsynopsis
openssl_csr_export_to_file(OpenSSLCertificateSigningRequest|string $csr, string $output_filename, bool $no_text = true): bool
```

**opensslcsrexportтоfile()** записує запит на підпис сертифіката `csr` у форматі PEM у файл `output_filename`

### Список параметрів

`csr`

Для отримання списку допустимих значень дивіться [параметри CSR](openssl.certparams.md)

`output_filename`

Шлях до файлу.

`no_text`

Необов'язковий параметр `notext` впливає на деталізацію повідомлень виводу; якщо він встановлений у **`false`**, то у висновок додається додаткова людиночитана інформація. Значення за замовчуванням `notext` є **`true`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `csr` тепер приймає екземпляр [OpenSSLCertificateSigningRequest](class.opensslcertificatesigningrequest.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу `OpenSSL X.509 CSR` |

### Приклади

**Приклад #1 Приклад використання opensslcsrexportтоfile()**

```php
<?php
$subject = array(
    "commonName" => "example.com",
);
$private_key = openssl_pkey_new(array(
    "private_key_bits" => 2048,
    "private_key_type" => OPENSSL_KEYTYPE_RSA,
));
$csr = openssl_csr_new($subject, $private_key, array('digest_alg' => 'sha384') );
openssl_pkey_export_to_file($private_key, 'example-priv.key');
// Наряду с объектом, CSR содержит открытый ключ, соответствующий секретному ключу
openssl_csr_export_to_file($csr, 'example-csr.pem');
?>
```

### Дивіться також

-   [opensslcsrexport()](function.openssl-csr-export.md) - Експортує CSR у вигляді рядка
-   [opensslcsrnew()](function.openssl-csr-new.md) - Генерує CSR
-   [opensslcsrsign()](function.openssl-csr-sign.md) - Підписати CSR за допомогою іншого сертифіката (або ним же) та створити сертифікат
