---
navigation:
  - function.openssl-x509-checkpurpose.md: « openssl\_x509\_checkpurpose
  - function.openssl-x509-export.md: openssl\_x509\_export »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_x509\_export\_to\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_x509\_export\_to\_file

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

openssl\_x509\_export\_to\_file — Експортує сертифікат у файл

### Опис

```methodsynopsis
openssl_x509_export_to_file(OpenSSLCertificate|string $certificate, string $output_filename, bool $no_text = true): bool
```

\*\*openssl\_x509\_export\_to\_file()\*\*сохраняет сертификат`certificate` у файл `output_filename` у вигляді рядка у форматі PEM.

### Список параметрів

`x509`

Для списку коректних значень дивіться [Параметри ключів/сертифікатів](openssl.certparams.md)

`output_filename`

Шлях до файлу.

`no_text`

Необов'язковий параметр `notext` впливає на деталізацію повідомлень виводу; якщо він встановлений у **`false`**, то у висновок додається додаткова людиночитана інформація. Значення за замовчуванням `notext`является\*\*`true`\*\*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL X.509` |
