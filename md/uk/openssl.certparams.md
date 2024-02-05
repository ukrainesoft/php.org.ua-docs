---
navigation:
  - openssl.constants.other.md: « Інші константи
  - openssl.cert.verification.md: Перевірка сертифікатів »
  - index.md: PHP Manual
  - book.openssl.md: OpenSSL
title: Параметри ключа/сертифіката
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Параметри ключа/сертифіката

Деякі функції openssl потребують параметрів у вигляді ключа або сертифіката. Можна використовувати один із таких варіантів:

-   Сертифікати
    
    1.  Екземпляр [OpenSSLCertificate](class.opensslcertificate.md)(або до PHP 8.0.0 ресурс ([resource](language.types.resource.md)) типу`OpenSSL X.509`), що повертається функцією[openssl\_x509\_read()](function.openssl-x509-read.md)
    2.  Рядок формату file://path/to/cert.pem; Цей файл повинен містити сертифікат у форматі PEM.
    3.  Рядок, в якому знаходиться вміст сертифіката/ключа, закодованого PEM, може починатися з`-----BEGIN CERTIFICATE-----`
-   Запити підпису сертифіката (Certificate Signing Requests або CSRs)
    
    1.  Екземпляр [OpenSSLCertificateSigningRequest](class.opensslcertificatesigningrequest.md)(або до PHP 8.0.0 ресурс ([resource](language.types.resource.md)) типу`OpenSSL X.509 CSR`), що повертається функцією[openssl\_csr\_new()](function.openssl-csr-new.md)
    2.  Рядок виду file://path/to/csr.pem; Цей файл повинен містити CSR у форматі PEM.
    3.  Рядок з CSR, кодований у форматі PEM, повинен починатися з`-----BEGIN CERTIFICATE REQUEST-----`
-   Відкриті/закриті ключі
    
    1.  Екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md)(або до PHP 8.0.0 ресурс ([resource](language.types.resource.md)) типу`OpenSSL key`), що повертається функцією[openssl\_get\_publickey()](function.openssl-get-publickey.md) або [openssl\_get\_privatekey()](function.openssl-get-privatekey.md)
    2.  Тільки для відкритих ключів: екземпляр[OpenSSLCertificate](class.opensslcertificate.md)(або до PHP 8.0.0 ресурс ([resource](language.types.resource.md)) типу`OpenSSL X.509`) .
    3.  Рядок формату file://path/to/file.pem - вказаний файл повинен містити сертифікат у форматі PEM (може містити обидва ключі).
    4.  Рядок, в якому знаходиться вміст сертифіката/ключа, закодованого PEM, може починатися з`-----BEGIN CERTIFICATE-----`
    5.  Для закритих ключів можливе використання синтаксису`array($key, $passphrase)`де $key представляє ключ вказаний за допомогою формату file:// або текстовий вміст описаний вище, а $passphrase представляє рядок, що містить пароль для зазначеного закритого ключа
