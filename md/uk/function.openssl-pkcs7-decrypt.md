---
navigation:
  - function.openssl-pkcs12-read.md: « opensslpkcs12read
  - function.openssl-pkcs7-encrypt.md: opensslpkcs7encrypt »
  - index.md: PHP Manual
  - ref.openssl.md: Функции OpenSSL
title: opensslpkcs7decrypt
---
# opensslpkcs7decrypt

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

opensslpkcs7decrypt — Розшифрувати повідомлення, зашифроване S/MIME

### Опис

```methodsynopsis
openssl_pkcs7_decrypt(    string $input_filename,    string $output_filename,    OpenSSLCertificate|string $certificate,    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string|null $private_key = null): bool
```

Розшифровує повідомлення, зашифроване S/MIME, що міститься у файлі `input_filename`, з використанням сертифіката `certificate` та відповідного закритого ключа `private_key`

### Список параметрів

`input_filename`

`output_filename`

Розшифроване повідомлення буде записано у файл `output_filename`

`certificate`

`private_key`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `private_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу `OpenSSL key` або `OpenSSL X.509 CSR` |

### Приклади

**Приклад #1 Приклад використання **opensslpkcs7decrypt()****

```php
<?php
// $cert и $key содержат пару с личным сертификатом и закрытым ключом
$infilename = "encrypted.msg";  // в этом файле зашифрованное сообщение
$outfilename = "decrypted.msg"; // убедитесь, что у вас есть права на запись

if (openssl_pkcs7_decrypt($infilename, $outfilename, $cert, $key)) {
    echo "расшифровано!";
} else {
    echo "возникла ошибка при расшифровке!";
}
?>
```
