---
navigation:
  - function.openssl-x509-read.md: « openssl\_x509\_read
  - class.opensslcertificate.md: OpenSSLCertificate »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_x509\_verify
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_x509\_verify

(PHP 7 >= 7.4.0, PHP 8)

openssl\_x509\_verify — Перевірити цифровий підпис сертифіката x509 за допомогою публічного ключа

### Опис

```methodsynopsis
openssl_x509_verify(OpenSSLCertificate|string $certificate, OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $public_key): int
```

**openssl\_x509\_verify()** перевіряє, що сертифікат `certificate` був підписаний приватним ключем, що відповідає публічному ключу `public_key`

### Список параметрів

`x509`

Для списку коректних значень дивіться [Параметри ключів/сертифікатів](openssl.certparams.md)

`public_key`

[OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) - ключ, повернутий функцією [openssl\_get\_publickey()](function.openssl-get-publickey.md)

string - ключ у форматі PEM, такого виду: `-----BEGIN PUBLIC KEY----- MIIBCgK...`

### Значення, що повертаються

Повертає 1, якщо підпис коректний, 0, якщо ні, та -1 у разі виникнення помилки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL X.509` |
| 8.0.0 | `public_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL key`или`OpenSSL X.509` |

### Приклади

**Пример #1 Пример использования**openssl\_x509\_verify()\*\*\*\*

```php
<?php
$hostname = "news.php.net";
$ssloptions = array(
    "capture_peer_cert" => true,
    "capture_peer_cert_chain" => true,
    "allow_self_signed"=> false,
    "CN_match" => $hostname,
    "verify_peer" => true,
    "SNI_enabled" => true,
    "SNI_server_name" => $hostname,
);

$ctx = stream_context_create( array("ssl" => $ssloptions) );
$result = stream_socket_client("ssl://$hostname:443", $errno, $errstr, 30, STREAM_CLIENT_CONNECT, $ctx);
$cont = stream_context_get_params($result);
$x509 = $cont["options"]["ssl"]["peer_certificate"];
$certparsed = openssl_x509_parse($x509);

foreach($cont["options"]["ssl"]["peer_certificate_chain"] as $chaincert)
{
    $chainparsed = openssl_x509_parse($chaincert);
    $chain_public_key = openssl_get_publickey($chaincert);
    $r = openssl_x509_verify($x509, $chain_public_key);
    if ($r==1)
    {
        echo $certparsed['subject']['CN'];
        echo " was digitally signed by ";
        echo $chainparsed['subject']['CN']."\n";
    }
}
?>
```

### Дивіться також

-   [openssl\_verify()](function.openssl-verify.md) \- Звіряння сигнатури
-   [openssl\_get\_publickey()](function.openssl-get-publickey.md) \- Псевдонім openssl\_pkey\_get\_public
