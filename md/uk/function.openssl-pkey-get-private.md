---
navigation:
  - function.openssl-pkey-get-details.md: « openssl\_pkey\_get\_details
  - function.openssl-pkey-get-public.md: openssl\_pkey\_get\_public »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_pkey\_get\_private
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_pkey\_get\_private

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

openssl\_pkey\_get\_private — Отримати закритий ключ

### Опис

```methodsynopsis
openssl_pkey_get_private(OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $private_key, ?string $passphrase = null): OpenSSLAsymmetricKey|false
```

**openssl\_pkey\_get\_private()** розбирає `private_key` та готує його до використання в інших функціях.

### Список параметрів

`private_key`

`private_key` може бути заданий наступним чином:

1.  рядок виду file://path/to/file.pem. Файл повинен містити кодований у PEM сертифікат/закритий ключ (може містити те й інше).
2.  Секретний ключ у форматі PEM.

`passphrase`

Якщо ключ захищений паролем, його треба вказати в параметрі `passphrase`

### Значення, що повертаються

Повертає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md)или\*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція повертає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md); раніше повертався ресурс ([resource](language.types.resource.md)) типу`OpenSSL key` |
| 8.0.0 | `private_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL key`или`OpenSSL X.509` |
| 8.0.0 | `passphrase` тепер допускає значення null. |
