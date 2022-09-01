---
navigation:
  - function.openssl-seal.html: « opensslseal
  - function.openssl-spki-export-challenge.html: opensslspkiexportchallenge »
  - index.html: PHP Manual
  - ref.openssl.html: Функции OpenSSL
title: opensslsign
---
# opensslsign

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

opensslsign — Генерація підпису

### Опис

```methodsynopsis
openssl_sign(    string $data,    string &$signature,    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $private_key,    string|int $algorithm = OPENSSL_ALGO_SHA1): bool
```

**opensslsign()** обчислює підпис даних `data` шляхом генерації криптографічного цифрового зліпка з використанням секретного ключа `private_key`. Зверніть увагу, що дані не шифруються.

### Список параметрів

`data`

Рядок даних, для яких ви хочете отримати відбиток

`signature`

Якщо функція відпрацює успішно, то підпис буде поміщений у змінну, задану в `signature`

`private_key`

Ідентифікатор ключа типу [OpenSSLAsymmetricKey](class.opensslasymmetrickey.html), отриманий з [opensslgetprivatekey()](function.openssl-get-privatekey.html)

Рядок, що є ключем у форматі PEM

`algorithm`

Ціле число, що визначає алгоритм. Дивіться [алгоритми підпису](openssl.signature-algos.html)

Рядок, повернутий [opensslgetмдmethods()](function.openssl-get-md-methods.html). Наприклад, "sha256WithRSAEncryption" або "sha384".

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `private_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.html) або [OpenSSLCertificate](class.opensslcertificate.html); раніше приймався ресурс ([resource](language.types.resource.html)) типу `OpenSSL key` або `OpenSSL X.509` |

### Приклади

**Приклад #1 Приклад використання **opensslsign()****

```php
<?php
// $data содержит данные для генерации подписи

// Извлекаем секретный ключ из файла и подготавливаем
$pkeyid = openssl_pkey_get_private("file://src/openssl-0.9.6/demos/sign/key.pem");

// Вычисляем подпись
openssl_sign($data, $signature, $pkeyid);

// Высвобождаем ресурс ключа
openssl_free_key($pkeyid);
?>
```

**Приклад #2 Приклад використання **opensslsign()****

```php
<?php
//Данные для генерации сигнатуры
$data = 'my data';

//Создаём новую пару открытый/закрытый ключ
$new_key_pair = openssl_pkey_new(array(
    "private_key_bits" => 2048,
    "private_key_type" => OPENSSL_KEYTYPE_RSA,
));
openssl_pkey_export($new_key_pair, $private_key_pem);

$details = openssl_pkey_get_details($new_key_pair);
$public_key_pem = $details['key'];

//Вычисляем подпись
openssl_sign($data, $signature, $private_key_pem, OPENSSL_ALGO_SHA256);

//Сохраняем
file_put_contents('private_key.pem', $private_key_pem);
file_put_contents('public_key.pem', $public_key_pem);
file_put_contents('signature.dat', $signature);

//Сверяем подпись
$r = openssl_verify($data, $signature, $public_key_pem, "sha256WithRSAEncryption");
var_dump($r);
?>
```

### Дивіться також

-   [opensslverify()](function.openssl-verify.html) - Звіряння сигнатури
