---
navigation:
  - function.openssl-spki-verify.md: « openssl\_spki\_verify
  - function.openssl-x509-check-private-key.md: openssl\_x509\_check\_private\_key »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_verify
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_verify

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

openssl\_verify - Звіряння сигнатури

### Опис

```methodsynopsis
openssl_verify(    string $data,    string $signature,    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $public_key,    string|int $algorithm = OPENSSL_ALGO_SHA1): int|false
```

**openssl\_verify()** перевіряє, що підпис `signature` коректна для даних `data` та відкритого ключа `public_key`. Відкритий ключ повинен відповідати закритому ключу, за допомогою якого генерувався підпис.

### Список параметрів

`data`

Перевірені дані

`signature`

Необроблений бінарний рядок, створений функцією [openssl\_sign()](function.openssl-sign.md) або її аналогом

`public_key`

Переменная типа[OpenSSLAsymmetricKey](class.opensslasymmetrickey.md), що містить ключ, підготовлений [openssl\_get\_publickey()](function.openssl-get-publickey.md)

Рядок із ключем у форматі PEM. Приблизно такого виду `-----BEGIN PUBLIC KEY----- MIIBCgK...`

`algorithm`

Целое число, соответствующее одному из[алгоритмів підпису](openssl.signature-algos.md)

Рядок, повернутий [openssl\_get\_md\_methods()](function.openssl-get-md-methods.md)наприклад "sha1WithRSAEncryption" або "sha512".

### Значення, що повертаються

Повертає 1, якщо підпис коректний, 0, якщо ні та -1 або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `public_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL key`или`OpenSSL X.509` |

### Приклади

**Пример #1 Пример использования**openssl\_verify()\*\*\*\*

```php
<?php
// $data и $signature содержат данные и подпись соответственно

// Извлекает открытый ключ из сертификата и подготавливаем его
$pubkeyid = openssl_pkey_get_public("file://src/openssl-0.9.6/demos/sign/cert.pem");

// Проверяем, корректна ли подпись
$ok = openssl_verify($data, $signature, $pubkeyid);
if ($ok == 1) {
    echo "Подпись корректная";
} elseif ($ok == 0) {
    echo "Подпись некорректная";
} else {
    echo "Произошла какая-то ошибка, печаль :(";
}
// Удаляем ключ из памяти
openssl_free_key($pubkeyid);
?>
```

**Пример #2 Пример использования**openssl\_verify()\*\*\*\*

```php
<?php
//Данные для генерации подписи
$data = 'my data';

//Создаём новую пару открытый/закрытый ключ
$private_key_res = openssl_pkey_new(array(
    "private_key_bits" => 2048,
    "private_key_type" => OPENSSL_KEYTYPE_RSA,
));
$details = openssl_pkey_get_details($private_key_res);
$public_key_res = openssl_pkey_get_public($details['key']);

//Вычисляем подпись
openssl_sign($data, $signature, $private_key_res, "sha256WithRSAEncryption");

//Сверяем подпись
$ok = openssl_verify($data, $signature, $public_key_res, OPENSSL_ALGO_SHA256);
if ($ok == 1) {
    echo "корректна";
} elseif ($ok == 0) {
    echo "некорректна";
} else {
    echo "ошибка: ".openssl_error_string();
}
?>
```

### Дивіться також

-   [openssl\_sign()](function.openssl-sign.md) \- генерація підпису
