---
navigation:
  - function.openssl-x509-export-to-file.md: « openssl\_x509\_export\_to\_file
  - function.openssl-x509-fingerprint.md: openssl\_x509\_fingerprint »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_x509\_export
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_x509\_export

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

openssl\_x509\_export — Експортує сертифікат у рядок

### Опис

```methodsynopsis
openssl_x509_export(OpenSSLCertificate|string $certificate, string &$output, bool $no_text = true): bool
```

\*\*openssl\_x509\_export()\*\*сохраняет сертификат`certificate` у вигляді PEM рядка в `output`

### Список параметрів

`x509`

Для списку коректних значень дивіться [Параметри ключів/сертифікатів](openssl.certparams.md)

`output`

У разі успішного виконання цієї змінної буде PEM-подання сертифіката.

`no_text`

Необов'язковий параметр `notext` впливає на деталізацію повідомлень виводу; якщо він встановлений у **`false`**, то у висновок додається додаткова людиночитана інформація. Значення за замовчуванням `notext`является\*\*`true`\*\*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL X.509` |
