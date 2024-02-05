---
navigation:
  - function.openssl-get-publickey.md: « openssl\_get\_publickey
  - function.openssl-pbkdf2.md: openssl\_pbkdf2 »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_open
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_open

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

openssl\_open — Відкрити запечатані дані

### Опис

```methodsynopsis
openssl_open(    string $data,    string &$output,    string $encrypted_key,    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $private_key,    string $cipher_algo,    ?string $iv = null): bool
```

**openssl\_open()** відкриває (дешифрує) `data`, використовуючи секретний ключ, пов'язаний з ідентифікатором `private_key` і ключ обгортки `encrypted_key`, і заповнює `output` розшифрованими даними. Ключ обгортки створюється під час запечатування даних і може використовуватися тільки з одним секретним ключем. Докладніше можна прочитати на сторінці опису функції [openssl\_seal()](function.openssl-seal.md)

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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `private_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL key`или`OpenSSL X.509 CSR` |
| 8.0.0 | `cipher_algo` більше не є необов'язковим параметром. |

### Приклади

**Пример #1 Пример использования**openssl\_open()\*\*\*\*

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

-   [openssl\_seal()](function.openssl-seal.md) \- Запечатати (зашифрувати) дані
