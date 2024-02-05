---
navigation:
  - function.openssl-csr-export-to-file.md: « openssl\_csr\_export\_to\_file
  - function.openssl-csr-get-public-key.md: openssl\_csr\_get\_public\_key »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_csr\_export
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_csr\_export

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

openssl\_csr\_export — Експортує CSR у вигляді рядка

### Опис

```methodsynopsis
openssl_csr_export(OpenSSLCertificateSigningRequest|string $csr, string &$output, bool $no_text = true): bool
```

**openssl\_csr\_export()** записує запит на підпис сертифіката `csr`в формате PEM в переменную`output`, яка передається за посиланням.

### Список параметрів

`csr`

Для отримання списку допустимих значень дивіться [параметри CSR](openssl.certparams.md)

`output`

У разі успішного виконання, у цій змінній буде збережено CSR у форматі PEM.

`no_text`

Необов'язковий параметр `notext` впливає на деталізацію повідомлень виводу; якщо він встановлений у **`false`**, то у висновок додається додаткова людиночитана інформація. Значення за замовчуванням `notext`является\*\*`true`\*\*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `csr` тепер приймає екземпляр [OpenSSLCertificateSigningRequest](class.opensslcertificatesigningrequest.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL X.509 CSR` |

### Приклади

**Приклад #1 Приклад використання openssl\_csr\_export()**

```php
<?php
$subject = array(
    "commonName" => "example.com",
);
$private_key = openssl_pkey_new(array(
    "private_key_bits" => 2048,
    "private_key_type" => OPENSSL_KEYTYPE_RSA,
));
$configargs = array(
    'digest_alg' => 'sha256WithRSAEncryption'
);
$csr = openssl_csr_new($subject, $private_key, $configargs);
openssl_csr_export($csr, $csr_string);
echo $csr_string;
?>
```

### Дивіться також

-   [openssl\_csr\_export\_to\_file()](function.openssl-csr-export-to-file.md) \- Експортує CSR у файл
-   [openssl\_csr\_new()](function.openssl-csr-new.md) \- Генерує CSR
-   [openssl\_csr\_sign()](function.openssl-csr-sign.md) \- Підписати CSR за допомогою іншого сертифіката (або ним же) та створити сертифікат
