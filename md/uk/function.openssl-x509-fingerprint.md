---
navigation:
  - function.openssl-x509-export.md: « openssl\_x509\_export
  - function.openssl-x509-free.md: openssl\_x509\_free »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_x509\_fingerprint
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_x509\_fingerprint

(PHP 5 >= 5.6.0, PHP 7, PHP 8)

openssl\_x509\_fingerprint — обчислює відбиток або дайджест, заданий сертифікатом X.509

### Опис

```methodsynopsis
openssl_x509_fingerprint(OpenSSLCertificate|string $certificate, string $digest_algo = "sha1", bool $binary = false): string|false
```

**openssl\_x509\_fingerprint()** повертає дайджест `certificate` у вигляді рядка.

### Список параметрів

`x509`

Для списку коректних значень дивіться [Параметри ключів/сертифікатів](openssl.certparams.md)

`digest_algo`

Метод хешування. Список доступних методів можна отримати за допомогою [openssl\_get\_md\_methods()](function.openssl-get-md-methods.md)

`binary`

Если установлено как\*\*`true`\*\*, буде повернуто необроблені бінарні дані. Якщо **`false`**, то виводить рядок із шістнадцяткових чисел у нижньому регістрі.

### Значення, що повертаються

Повертає відбиток сертифіката у вигляді рядка шістнадцяткових чисел. Якщо `binary`установлен в\*\*`true`\*\*то у вигляді бінарних даних.

У разі виникнення помилки повертає **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL X.509` |
