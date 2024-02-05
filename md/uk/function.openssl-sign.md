---
navigation:
  - function.openssl-seal.md: « openssl\_seal
  - function.openssl-spki-export-challenge.md: openssl\_spki\_export\_challenge »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_sign
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_sign

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

openssl\_sign — Генерація підпису

### Опис

```methodsynopsis
openssl_sign(    string $data,    string &$signature,    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $private_key,    string|int $algorithm = OPENSSL_ALGO_SHA1): bool
```

**openssl\_sign()** обчислює підпис даних `data` шляхом генерації криптографічного цифрового зліпка з використанням секретного ключа `private_key`. Зверніть увагу, що дані не шифруються.

### Список параметрів

`data`

Рядок даних, для яких ви хочете отримати відбиток

`signature`

Якщо функція відпрацює успішно, то підпис буде поміщений у змінну, задану в `signature`

`private_key`

Ідентифікатор ключа типу [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md), отриманий з [openssl\_get\_privatekey()](function.openssl-get-privatekey.md)

Рядок, що є ключем у форматі PEM.

`algorithm`

Целое число, определяющее алгоритм. Смотрите[алгоритми підпису](openssl.signature-algos.md)

Рядок, повернутий [openssl\_get\_md\_methods()](function.openssl-get-md-methods.md). . Наприклад, "sha256WithRSAEncryption" або "sha384".

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `private_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL key`или`OpenSSL X.509` |

### Приклади

**Пример #1 Пример использования**openssl\_sign()\*\*\*\*

```php
<?php
// $data содержит данные для генерации подписи

// Извлекаем секретный ключ из файла и подготавливаем
$pkeyid = openssl_pkey_get_private("file://src/openssl-0.9.6/demos/sign/key.pem");

// Вычисляем подпись
openssl_sign($data, $signature, $pkeyid);

// Высвобождаем ресурс ключа
openssl_free_key($pkeyid);
?>
```

**Пример #2 Пример использования**openssl\_sign()\*\*\*\*

```php
<?php
//Данные для генерации сигнатуры
$data = 'my data';

//Создаём новую пару открытый/закрытый ключ
$new_key_pair = openssl_pkey_new(array(
    "private_key_bits" => 2048,
    "private_key_type" => OPENSSL_KEYTYPE_RSA,
));
openssl_pkey_export($new_key_pair, $private_key_pem);

$details = openssl_pkey_get_details($new_key_pair);
$public_key_pem = $details['key'];

//Вычисляем подпись
openssl_sign($data, $signature, $private_key_pem, OPENSSL_ALGO_SHA256);

//Сохраняем
file_put_contents('private_key.pem', $private_key_pem);
file_put_contents('public_key.pem', $public_key_pem);
file_put_contents('signature.dat', $signature);

//Сверяем подпись
$r = openssl_verify($data, $signature, $public_key_pem, "sha256WithRSAEncryption");
var_dump($r);
?>
```

### Дивіться також

-   [openssl\_verify()](function.openssl-verify.md) \- Звіряння сигнатури
