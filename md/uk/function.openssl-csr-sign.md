---
navigation:
  - function.openssl-csr-new.md: « opensslcsrnew
  - function.openssl-decrypt.md: openssldecrypt »
  - index.md: PHP Manual
  - ref.openssl.md: Функции OpenSSL
title: opensslcsrsign
---
# opensslcsrsign

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

opensslcsrsign — Підписати CSR за допомогою іншого сертифіката (або їм) і створити сертифікат

### Опис

```methodsynopsis
openssl_csr_sign(    OpenSSLCertificateSigningRequest|string $csr,    OpenSSLCertificate|string|null $ca_certificate,    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $private_key,    int $days,    ?array $options = null,    int $serial = 0): OpenSSLCertificate|false
```

**opensslcsrsign()** створює сертифікат x509 із заданого CSR.

> **Зауваження**: Для коректної роботи цієї функції має бути правильний openssl.cnf. Для більш детальної інформації дивіться зауваження під [разделом установки](openssl.installation.md)

### Список параметрів

`csr`

Створений за допомогою [opensslcsrnew()](function.openssl-csr-new.md) CSR. Також може бути шляхом кодованого в PEM CSR, якщо задано як file://path/to/csr або експортованим рядком, створеним за допомогою [opensslcsrexport()](function.openssl-csr-export.md)

`ca_certificate`

Створюваний сертифікат буде підписано `ca_certificate`. Якщо `ca_certificate` заданий як **`null`**, буде згенерований самопідписаний сертифікат.

`private_key`

`private_key` - секретний ключ, відповідний `ca_certificate`

`days`

`days` - час життя сертифіката, що створюється, в днях.

`options`

Можна тонко налаштувати підпис CSR за допомогою `options`. Подробиці дивіться в описі функції [opensslcsrnew()](function.openssl-csr-new.md), у розділі присвяченому параметру `options`

`serial`

Опційний серійний номер сертифіката, що випускається. Якщо не вказано, за промовчанням буде використано 0.

### Значення, що повертаються

Повертає [OpenSSLCertificate](class.opensslcertificate.md) у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | On success, this function returns an [OpenSSLCertificate](class.opensslcertificate.md) instance now; previously, a [resource](language.types.resource.md) of type `OpenSSL X.509` був returned. |
|  | `csr` тепер приймає екземпляр [OpenSSLCertificateSigningRequest](class.opensslcertificatesigningrequest.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу `OpenSSL X.509 CSR` |
|  | `ca_certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу `OpenSSL X.509 CSR` |
|  | `private_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу `OpenSSL X.509 CSR` |

### Приклади

**Приклад #1 Приклад **opensslcsrsign()** - підпис CSR (як зробити свій власний CA)**

```php
<?php
// Предположим, что CSR получен из поля textarea со веб-страницы
$csrdata = $_POST["CSR"];

// Мы подпишем запрос с помощью сертификата собственного "центра сертификации"
// Для подписи вы можете использовать любой сертификат, но этот процесс бесполезен, если
// сертификат не является доверенным для ПО или пользователей, которые будут его
// использовать

// Нам нужен собственный CA сертификат и его секретный ключ
$cacert = "file://path/to/ca.crt";
$privkey = array("file://path/to/ca.key", "your_ca_key_passphrase");

$usercert = openssl_csr_sign($csrdata, $cacert, $privkey, 365, array('digest_alg'=>'sha256') );

// Теперь напечатаем сертификат, чтобы пользователь мог его скопировать
// и внести в свою локальную конфигурацию (например в файл хранилища SSL сертификатов)
openssl_x509_export($usercert, $certout);
echo $certout;

// Покажем возникшие ошибки, если они были
while (($e = openssl_error_string()) !== false) {
    echo $e . "\n";
}
?>
```
