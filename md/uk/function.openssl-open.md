---
navigation:
  - function.openssl-get-publickey.md: « opensslgetpublickey
  - function.openssl-pbkdf2.md: opensslpbkdf2 »
  - index.md: PHP Manual
  - ref.openssl.md: Функции OpenSSL
title: opensslopen
---
# opensslopen

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

opensslopen — Відкрити запечатані дані

### Опис

```methodsynopsis
openssl_open(    string $data,    string &$output,    string $encrypted_key,    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $private_key,    string $cipher_algo,    ?string $iv = null): bool
```

**opensslopen()** відкриває (дешифрує) `data`, використовуючи секретний ключ, пов'язаний з ідентифікатором `private_key` і ключ обгортки `encrypted_key`, і заповнює `output` розшифрованими даними. Ключ обгортки створюється під час запечатування даних і може використовуватися тільки з одним секретним ключем. Докладніше можна прочитати на сторінці опису функції [opensslseal()](function.openssl-seal.md)

### Список параметрів

`data`

`output`

При вдалому завершенні змінна передана в цьому параметрі міститиме відкриті дані.

`encrypted_key`

`private_key`

`cipher_algo`

Метод шифрування.

**Застереження**

Значення за замовчуванням (`'RC4'`) вважається небезпечним. Настійно рекомендується вказувати метод безпечного шифрування.

`iv`

Ініціалізуючий вектор.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `private_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу `OpenSSL key` або `OpenSSL X.509 CSR` |
|  | `cipher_algo` більше не є необов'язковим параметром. |

### Приклади

**Приклад #1 Приклад використання **opensslopen()****

```php
<?php
// Предположим, что $sealed и $env_key содержат закрытые данные и
// ключ обёртки соответственно

// Извлекаем секретный ключ из файла
$fp = fopen("/src/openssl-0.9.6/demos/sign/key.pem", "r");
$priv_key = fread($fp, 8192);
fclose($fp);
$pkeyid = openssl_get_privatekey($priv_key);

// расшмфровываем данные и складываем их в $open
if (openssl_open($sealed, $open, $env_key, $pkeyid)) {
    echo "Расшифрованные данные: ", $open;
} else {
    echo "Что-то пошло не так :(";
}

// Высвобождаем ресурс приватнного ключа
openssl_free_key($pkeyid);
?>
```

### Дивіться також

-   [opensslseal()](function.openssl-seal.md) - Запечатати (зашифрувати) дані
