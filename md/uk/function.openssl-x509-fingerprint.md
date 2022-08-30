Обчислює відбиток або дайджест, заданий сертифікатом X.509

-   [« opensslx509export](function.openssl-x509-export.html)
    
-   [opensslx509free »](function.openssl-x509-free.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Обчислює відбиток або дайджест, заданий сертифікатом X.509
    

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

Для списку коректних значень дивіться [Параметры ключей/сертификатов](openssl.certparams.html)

`digest_algo`

Метод хешування. Список доступних методів можна отримати за допомогою [opensslgetмдmethods()](function.openssl-get-md-methods.html)

`binary`

Якщо встановлено як **`true`**, буде повернуто необроблені бінарні дані. Якщо **`false`**, то виводить рядок із шістнадцяткових чисел у нижньому регістрі.

### Значення, що повертаються

Повертає відбиток сертифіката у вигляді рядка шістнадцяткових чисел. Якщо `binary` встановлений в \*\*`true`\*\*то у вигляді бінарних даних.

У разі виникнення помилки повертає **`false`**

### список змін

| Версия | Описание                                                                                                                                                                           |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.html); раніше приймався ресурс ([resource](language.types.resource.html)) типу `OpenSSL X.509` |