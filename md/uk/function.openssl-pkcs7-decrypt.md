---
navigation:
  - function.openssl-pkcs12-read.md: « openssl\_pkcs12\_read
  - function.openssl-pkcs7-encrypt.md: openssl\_pkcs7\_encrypt »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_pkcs7\_decrypt
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_pkcs7\_decrypt

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

openssl\_pkcs7\_decrypt — Розшифрувати повідомлення, зашифроване S/MIME

### Опис

```methodsynopsis
openssl_pkcs7_decrypt(    string $input_filename,    string $output_filename,    OpenSSLCertificate|string $certificate,    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string|null $private_key = null): bool
```

Розшифровує повідомлення, зашифроване S/MIME, що міститься у файлі `input_filename`, с использованием сертификата`certificate` та відповідного закритого ключа `private_key`

### Список параметрів

`input_filename`

`output_filename`

Розшифроване повідомлення буде записано у файл `output_filename`

`certificate`

`private_key`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `private_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL key`или`OpenSSL X.509 CSR` |

### Приклади

**Пример #1 Пример использования**openssl\_pkcs7\_decrypt()\*\*\*\*

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
