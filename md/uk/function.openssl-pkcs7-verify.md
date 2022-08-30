Перевірити підпис повідомлення S/MIME

-   [« opensslpkcs7sign](function.openssl-pkcs7-sign.html)
    
-   [opensslpkeyderive »](function.openssl-pkey-derive.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OpenSSL](ref.openssl.html)
    
-   Перевірити підпис повідомлення S/MIME
    

# opensslpkcs7verify

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

opensslpkcs7verify — Перевірити підпис повідомлення S/MIME

### Опис

```methodsynopsis
openssl_pkcs7_verify(    string $input_filename,    int $flags,    ?string $signers_certificates_filename = null,    array $ca_info = [],    ?string $untrusted_certificates_filename = null,    ?string $content = null,    ?string $output_filename = null): bool|int
```

**opensslpkcs7verify()** читає S/MIME повідомлення з файлу та перевіряє його підпис.

### Список параметрів

`input_filename`

Шлях до файлу із повідомленням.

`flags`

`flags` можна використовувати модифікації процесу перевірки. Детальніше дивіться [константи PKCS7](openssl.pkcs7.flags.html)

`signers_certificates_filename`

Якщо встановлено параметр `signers_certificates_filename`, то в ньому має бути рядок з ім'ям файлу, в який будуть збережені сертифікати, використані під час підписання, у форматі PEM.

`ca_info`

Якщо встановлено параметр `ca_info`, то в ньому повинна бути інформація про довірені сертифікати CA, які необхідно використовувати в процесі перевірки. Докладніше читайте на сторінці [проверки сертификатов](openssl.cert.verification.html)

`untrusted_certificates_filename`

Якщо встановлено параметр `untrusted_certificates_filename`, у ньому має бути ім'я файлу, що містить набір недовірених сертифікатів CA.

`content`

У параметрі `content` можна вказати ім'я файлу, до якого буде записано верифіковані дані без інформації про підпис.

`output_filename`

### Значення, що повертаються

Повертає **`true`**, якщо перевірка успішна, \*\*`false`\*\*якщо немає і -1 у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                        |
|--------|---------------------------------------------------------------------------------------------------------------------------------|
|        | `signers_certificates_filename` `untrusted_certificates_filename` `content` і `output_filename` тепер допускають значення null. |
|        | Доданий параметр `output_filename`                                                                                              |

### Примітки

> **Зауваження**: Як зазначено в RFC 2045, довжина параметра `input_filename` не має бути довшим за 76 символів.