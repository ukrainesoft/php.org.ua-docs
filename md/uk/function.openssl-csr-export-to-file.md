---
navigation:
  - function.openssl-cms-verify.md: « openssl\_cms\_verify
  - function.openssl-csr-export.md: openssl\_csr\_export »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_csr\_export\_to\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_csr\_export\_to\_file

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

openssl\_csr\_export\_to\_file — Експортує CSR у файл

### Опис

```methodsynopsis
openssl_csr_export_to_file(OpenSSLCertificateSigningRequest|string $csr, string $output_filename, bool $no_text = true): bool
```

**openssl\_csr\_export\_to\_file()** записує запит на підпис сертифіката `csr`в формате PEM в файл`output_filename`

### Список параметрів

`csr`

Для отримання списку допустимих значень дивіться [параметри CSR](openssl.certparams.md)

`output_filename`

Шлях до файлу.

`no_text`

Необов'язковий параметр `notext` впливає на деталізацію повідомлень виводу; якщо він встановлений у **`false`**, то у висновок додається додаткова людиночитана інформація. Значення за замовчуванням `notext`является\*\*`true`\*\*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `csr` тепер приймає екземпляр [OpenSSLCertificateSigningRequest](class.opensslcertificatesigningrequest.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL X.509 CSR` |

### Приклади

**Приклад #1 Приклад використання openssl\_csr\_export\_to\_file()**

```php
<?php
$subject = array(
    "commonName" => "example.com",
);
$private_key = openssl_pkey_new(array(
    "private_key_bits" => 2048,
    "private_key_type" => OPENSSL_KEYTYPE_RSA,
));
$csr = openssl_csr_new($subject, $private_key, array('digest_alg' => 'sha384') );
openssl_pkey_export_to_file($private_key, 'example-priv.key');
// Наряду с объектом, CSR содержит открытый ключ, соответствующий секретному ключу
openssl_csr_export_to_file($csr, 'example-csr.pem');
?>
```

### Дивіться також

-   [openssl\_csr\_export()](function.openssl-csr-export.md) \- Експортує CSR у вигляді рядка
-   [openssl\_csr\_new()](function.openssl-csr-new.md) \- Генерує CSR
-   [openssl\_csr\_sign()](function.openssl-csr-sign.md) \- Підписати CSR за допомогою іншого сертифіката (або ним же) та створити сертифікат
