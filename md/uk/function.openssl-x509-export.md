---
navigation:
  - function.openssl-x509-export-to-file.md: « opensslx509exportтоfile
  - function.openssl-x509-fingerprint.md: opensslx509fingerprint »
  - index.md: PHP Manual
  - ref.openssl.md: Функции OpenSSL
title: opensslx509export
---
# opensslx509export

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

opensslx509export — Експортує сертифікат у рядок

### Опис

```methodsynopsis
openssl_x509_export(OpenSSLCertificate|string $certificate, string &$output, bool $no_text = true): bool
```

**opensslx509export()** зберігає сертифікат `certificate` у вигляді PEM рядка в `output`

### Список параметрів

`x509`

Для списку коректних значень дивіться [Параметри ключів/сертифікатів](openssl.certparams.md)

`output`

У разі успішного виконання цієї змінної буде PEM-представлення сертифіката.

`no_text`

Необов'язковий параметр `notext` впливає на деталізацію повідомлень виводу; якщо він встановлений у **`false`**, то у висновок додається додаткова людина читана інформація. Значення за замовчуванням `notext` є **`true`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу `OpenSSL X.509` |
