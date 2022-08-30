Розібрати сертифікат X.509 та повернути для нього об'єкт

-   [« opensslx509parse](function.openssl-x509-parse.html)
    
-   [opensslx509verify »](function.openssl-x509-verify.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Розібрати сертифікат X.509 та повернути для нього об'єкт
    

# opensslx509read

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

opensslx509read — Розібрати сертифікат X.509 та повернути для нього об'єкт

### Опис

```methodsynopsis
openssl_x509_read(OpenSSLCertificate|string $certificate): OpenSSLCertificate|false
```

**opensslx509read()** отримує сертифікат з `certificate` та повертає об'єкт [OpenSSLCertificate](class.opensslcertificate.html) для нього.

### Список параметрів

`certificate`

Сертифікат X509 Список коректних значень дивіться на сторінці [Параметри ключів та сертифікатів](openssl.certparams.html)

### Значення, що повертаються

Повертає об'єкт [OpenSSLCertificate](class.opensslcertificate.html) у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                                                    |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | У разі успішного виконання повертає екземпляр [OpenSSLCertificate](class.opensslcertificate.html); раніше повертався ресурс ([resource](language.types.resource.html)) типу `OpenSSL X.509` |
|        | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.html); раніше приймався ресурс ([resource](language.types.resource.html)) типу `OpenSSL X.509`          |