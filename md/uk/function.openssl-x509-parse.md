---
navigation:
  - function.openssl-x509-free.md: « openssl\_x509\_free
  - function.openssl-x509-read.md: openssl\_x509\_read »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_x509\_parse
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_x509\_parse

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

openssl\_x509\_parse — Розібрати сертифікат X509 та отримати масив з даними про нього

### Опис

```methodsynopsis
openssl_x509_parse(OpenSSLCertificate|string $certificate, bool $short_names = true): array|false
```

**openssl\_x509\_parse()** повертає інформацію сертифікату з ідентифікатором `certificate`включаючи такі поля, як ім'я суб'єкта, ім'я видавця, призначення, дати початку та закінчення дії і т.д.

### Список параметрів

`certificate`

Сертифікат X509 Список коректних значень дивись у [Параметри Key/Certificate](openssl.certparams.md)

`short_names`

`short_names` визначає, як індексуватимуться дані у підсумковому масиві. Якщо `short_names` поставити як **`true`** (за замовчуванням), поля будуть індексуватися короткими іменами, а не довгими. Наприклад, CN – це коротке ім'я для commonName.

### Значення, що повертаються

*Структура масива, що повертається, ще не до кінця встояла, так що поки не документується.*

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL X.509` |
