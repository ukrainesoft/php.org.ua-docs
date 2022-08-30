Звіряння сигнатури

-   [« opensslspkiverify](function.openssl-spki-verify.html)
    
-   [opensslx509checkprivatekey »](function.openssl-x509-check-private-key.html)
    
-   [PHP Manual](index.md)
    
-   [Функции OpenSSL](ref.openssl.md)
    
-   Звіряння сигнатури
    

# opensslverify

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

opensslverify - Звіряння сигнатури

### Опис

```methodsynopsis
openssl_verify(    string $data,    string $signature,    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $public_key,    string|int $algorithm = OPENSSL_ALGO_SHA1): int|false
```

**opensslverify()** перевіряє, що підпис `signature` коректна для даних `data` та відкритого ключа `public_key`. Відкритий ключ повинен відповідати закритому ключу, за допомогою якого генерувався підпис.

### Список параметрів

`data`

Перевірені дані

`signature`

Необроблений бінарний рядок, створений функцією [opensslsign()](function.openssl-sign.html) або її аналогом

`public_key`

Змінна типу [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md), що містить ключ, підготовлений [opensslgetpublickey()](function.openssl-get-publickey.html)

Рядок із ключем у форматі PEM. Приблизно такого виду "-----BEGIN PUBLIC KEY----- MIIBCgK..."

`algorithm`

Ціло число, що відповідає одному з [алгоритмов подписи](openssl.signature-algos.html)

Рядок, повернутий [opensslgetмдmethods()](function.openssl-get-md-methods.html)наприклад "sha1WithRSAEncryption" або "sha512".

### Значення, що повертаються

Повертає 1, якщо підпис коректний, 0, якщо ні та -1 або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                                                                                                                  |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | `public_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу `OpenSSL key` або `OpenSSL X.509` |

### Приклади

**Приклад #1 Приклад використання **opensslverify()****

```php
<?php
// $data и $signature содержат данные и подпись соответственно

// Извлекает открытый ключ из сертификата и подготавливаем его
$pubkeyid = openssl_pkey_get_public("file://src/openssl-0.9.6/demos/sign/cert.pem");

// Проверяем, корректна ли подпись
$ok = openssl_verify($data, $signature, $pubkeyid);
if ($ok == 1) {
    echo "Подпись корректная";
} elseif ($ok == 0) {
    echo "Подпись некорректная";
} else {
    echo "Произошла какая-то ошибка, печаль :(";
}
// Удаляем ключ из памяти
openssl_free_key($pubkeyid);
?>
```

**Приклад #2 Приклад використання **opensslverify()****

```php
<?php
//Данные для генерации подписи
$data = 'my data';

//Создаём новую пару открытый/закрытый ключ
$private_key_res = openssl_pkey_new(array(
    "private_key_bits" => 2048,
    "private_key_type" => OPENSSL_KEYTYPE_RSA,
));
$details = openssl_pkey_get_details($private_key_res);
$public_key_res = openssl_pkey_get_public($details['key']);

//Вычисляем подпись
openssl_sign($data, $signature, $private_key_res, "sha256WithRSAEncryption");

//Сверяем подпись
$ok = openssl_verify($data, $signature, $public_key_res, OPENSSL_ALGO_SHA256);
if ($ok == 1) {
    echo "корректна";
} elseif ($ok == 0) {
    echo "некорректна";
} else {
    echo "ошибка: ".openssl_error_string();
}
?>
```

### Дивіться також

-   [opensslsign()](function.openssl-sign.html) - генерація підпису