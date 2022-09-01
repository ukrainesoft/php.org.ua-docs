---
navigation:
  - function.openssl-pkey-get-details.html: « opensslpkeygetdetails
  - function.openssl-pkey-get-public.html: opensslpkeygetpublic »
  - index.md: PHP Manual
  - ref.openssl.md: Функции OpenSSL
title: opensslpkeygetprivate
---
# opensslpkeygetprivate

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

opensslpkeygetprivate — Отримати закритий ключ

### Опис

```methodsynopsis
openssl_pkey_get_private(OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $private_key, ?string $passphrase = null): OpenSSLAsymmetricKey|false
```

**opensslpkeygetprivate()** розбирає `private_key` та готує його до використання в інших функціях.

### Список параметрів

`private_key`

`private_key` може бути заданий наступним чином:

1.  рядок виду file://path/to/file.pem. Файл повинен містити кодований у PEM сертифікат/закритий ключ (може містити те й інше).
2.  Секретний ключ у форматі PEM.

`passphrase`

Якщо ключ захищений паролем, його треба вказати в параметрі `passphrase`

### Значення, що повертаються

Повертає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція повертає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md); раніше повертався ресурс ([resource](language.types.resource.md)) типу `OpenSSL key` |
|  | `private_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу `OpenSSL key` або `OpenSSL X.509` |
|  | `passphrase` тепер допускає значення null. |
