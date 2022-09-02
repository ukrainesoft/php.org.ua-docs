---
navigation:
  - function.openssl-x509-export.md: « opensslx509export
  - function.openssl-x509-free.md: opensslx509free »
  - index.md: PHP Manual
  - ref.openssl.md: Функции OpenSSL
title: opensslx509fingerprint
---
# opensslx509fingerprint

(PHP 5> = 5.6.0, PHP 7, PHP 8)

opensslx509fingerprint — обчислює відбиток або дайджест, заданий сертифікатом X.509

### Опис

```methodsynopsis
openssl_x509_fingerprint(OpenSSLCertificate|string $certificate, string $digest_algo = "sha1", bool $binary = false): string|false
```

**opensslx509fingerprint()** повертає дайджест `certificate` у вигляді рядка.

### Список параметрів

`x509`

Для списку коректних значень дивіться [Параметри ключів/сертифікатів](openssl.certparams.md)

`digest_algo`

Метод хешування. Список доступних методів можна отримати за допомогою [opensslgetмдmethods()](function.openssl-get-md-methods.md)

`binary`

Якщо встановлено як **`true`**, буде повернуто необроблені бінарні дані. Якщо **`false`**, то виводить рядок із шістнадцяткових чисел у нижньому регістрі.

### Значення, що повертаються

Повертає відбиток сертифіката у вигляді рядка шістнадцяткових чисел. Якщо `binary` встановлений в \*\*`true`\*\*то у вигляді бінарних даних.

У разі виникнення помилки повертає **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу `OpenSSL X.509` |
