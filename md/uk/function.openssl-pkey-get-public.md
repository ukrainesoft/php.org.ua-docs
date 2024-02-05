---
navigation:
  - function.openssl-pkey-get-private.md: « openssl\_pkey\_get\_private
  - function.openssl-pkey-new.md: openssl\_pkey\_new »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_pkey\_get\_public
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_pkey\_get\_public

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

openssl\_pkey\_get\_public — Витягує відкритий ключ із сертифікату та готує його до використання.

### Опис

```methodsynopsis
openssl_pkey_get_public(OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $public_key): OpenSSLAsymmetricKey|false
```

**openssl\_pkey\_get\_public()** витягує відкритий ключ з `public_key` та готує його до використання в інших функціях.

### Список параметрів

`public_key`

`public_key` може бути одним з:

1.  екземпляр[OpenSSLAsymmetricKey](class.opensslasymmetrickey.md)
2.  рядок виду file://path/to/file.pem. Файл повинен містити кодований у PEM сертифікат/публічний ключ (може містити і те, й інше).
3.  Відкритий ключ у форматі PEM.

### Значення, що повертаються

Повертає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md)или\*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання функція повертає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md); раніше повертався ресурс ([resource](language.types.resource.md)) типу`OpenSSL key` |
| 8.0.0 | `public_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL key`или`OpenSSL X.509` |
