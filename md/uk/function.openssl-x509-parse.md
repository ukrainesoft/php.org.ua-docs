Розібрати сертифікат X509 та отримати масив з даними про нього

-   [« opensslx509free](function.openssl-x509-free.html)
    
-   [opensslx509read »](function.openssl-x509-read.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Розібрати сертифікат X509 та отримати масив з даними про нього
    

# opensslx509parse

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

opensslx509parse — Розібрати сертифікат X509 та отримати масив з даними про нього

### Опис

```methodsynopsis
openssl_x509_parse(OpenSSLCertificate|string $certificate, bool $short_names = true): array|false
```

**opensslx509parse()** повертає інформацію сертифікату з ідентифікатором `certificate`, включаючи такі поля, як ім'я суб'єкта, ім'я видавця, призначення, дати початку та закінчення дії тощо.

### Список параметрів

`certificate`

Сертифікат X509 Список коректних значень дивись у [Параметри Key/Certificate](openssl.certparams.html)

`short_names`

`short_names` визначає, як індексуватимуться дані у підсумковому масиві. Якщо `short_names` поставити як **`true`** (за замовчуванням), поля будуть індексуватися короткими іменами, а не довгими. Наприклад, CN – це коротке ім'я для commonName.

### Значення, що повертаються

*Структура масива, що повертається, ще не до кінця встояла, так що поки не документується.*

### список змін

| Версия | Описание |
| --- | --- |
|  | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.html); раніше приймався ресурс ([resource](language.types.resource.html)) типу `OpenSSL X.509` |