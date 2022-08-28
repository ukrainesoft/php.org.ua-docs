Параметри ключа/сертифіката

-   [« Другие константы](openssl.constants.other.html)
    
-   [Проверка сертификатов »](openssl.cert.verification.html)
    
-   [PHP Manual](index.html)
    
-   [OpenSSL](book.openssl.html)
    
-   Параметри ключа/сертифіката
    

# Параметри ключа/сертифіката

Деякі функції openssl потребують параметрів у вигляді ключа або сертифіката. Можна використовувати один із таких варіантів:

-   Сертифікати
    
    1.  Екземпляр [OpenSSLCertificate](class.opensslcertificate.html) (або до PHP 8.0.0 ресурс ([resource](language.types.resource.html)) типу `OpenSSL X.509`), що повертається функцією [openssl\_x509\_read()](function.openssl-x509-read.html)
    2.  Рядок формату file://path/to/cert.pem; зазначений файл має містити сертифікат у форматі PEM
    3.  Рядок, в якому міститься вміст сертифіката/ключа, закодованого PEM
-   Запити підпису сертифіката (Certificate Signing Requests або CSRs)
    
    1.  Екземпляр [OpenSSLCertificateSigningRequest](class.opensslcertificatesigningrequest.html) (або до PHP 8.0.0 ресурс ([resource](language.types.resource.html)) типу `OpenSSL X.509 CSR`), що повертається функцією [openssl\_csr\_new()](function.openssl-csr-new.html)
    2.  Рядок виду file://path/to/csr.pem; вказаний файл повинен містити CSR у форматі PEM
    3.  Рядок з CSR, кодований у форматі PEM, повинен починатися з -----BEGIN CERTIFICATE REQUEST-----
-   Відкриті/закриті ключі
    
    1.  Екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.html) (або до PHP 8.0.0 ресурс ([resource](language.types.resource.html)) типу `OpenSSL key`), що повертається функцією [openssl\_get\_publickey()](function.openssl-get-publickey.html) або [openssl\_get\_privatekey()](function.openssl-get-privatekey.html)
    2.  Тільки для відкритих ключів: екземпляр [OpenSSLCertificate](class.opensslcertificate.html) (або до PHP 8.0.0 ресурс ([resource](language.types.resource.html)) типу `OpenSSL X.509`
    3.  Рядок формату file://path/to/file.pem - вказаний файл повинен містити сертифікат у форматі PEM (може містити обидва ключі)
    4.  Рядок, в якому міститься вміст сертифіката/ключа, закодованого PEM
    5.  Для закритих ключів можливе використання синтаксису `array($key, $passphrase)` де $key представляє ключ вказаний за допомогою формату file:// або текстовий вміст описаний вище, а $passphrase представляє рядок, що містить пароль для зазначеного закритого ключа