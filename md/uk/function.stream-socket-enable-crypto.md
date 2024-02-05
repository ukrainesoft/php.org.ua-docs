---
navigation:
  - function.stream-socket-client.md: « stream\_socket\_client
  - function.stream-socket-get-name.md: stream\_socket\_get\_name »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_socket\_enable\_crypto
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_socket\_enable\_crypto

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

stream\_socket\_enable\_crypto — Вмикає або вимикає шифрування на вже підключеному сокеті

### Опис

```methodsynopsis
stream_socket_enable_crypto(    resource $stream,    bool $enable,    ?int $crypto_method = null,    ?resource $session_stream = null): int|bool
```

Вмикає або вимикає шифрування на потоці.

Після налаштування шифрування, криптографія може бути увімкнена або вимкнена динамічно за допомогою передачі значення \*\*`true`** або **`false`\*\*параметру`enable`

### Список параметрів

`stream`

Потоковий ресурс.

`enable`

Увімкнути/вимкнути криптографію на потоці.

`crypto_method`

Увімкнути шифрування на потоці. Допустимі методи

-   **`STREAM_CRYPTO_METHOD_SSLv2_CLIENT`**
-   **`STREAM_CRYPTO_METHOD_SSLv3_CLIENT`**
-   **`STREAM_CRYPTO_METHOD_SSLv23_CLIENT`**
-   **`STREAM_CRYPTO_METHOD_ANY_CLIENT`**
-   **`STREAM_CRYPTO_METHOD_TLS_CLIENT`**
-   **`STREAM_CRYPTO_METHOD_TLSv1_0_CLIENT`**
-   **`STREAM_CRYPTO_METHOD_TLSv1_1_CLIENT`**
-   **`STREAM_CRYPTO_METHOD_TLSv1_2_CLIENT`**
-   **`STREAM_CRYPTO_METHOD_TLSv1_3_CLIENT`**(починаючи з PHP 7.4.0)
-   **`STREAM_CRYPTO_METHOD_SSLv2_SERVER`**
-   **`STREAM_CRYPTO_METHOD_SSLv3_SERVER`**
-   **`STREAM_CRYPTO_METHOD_SSLv23_SERVER`**
-   **`STREAM_CRYPTO_METHOD_ANY_SERVER`**
-   **`STREAM_CRYPTO_METHOD_TLS_SERVER`**
-   **`STREAM_CRYPTO_METHOD_TLSv1_0_SERVER`**
-   **`STREAM_CRYPTO_METHOD_TLSv1_1_SERVER`**
-   **`STREAM_CRYPTO_METHOD_TLSv1_2_SERVER`**
-   **`STREAM_CRYPTO_METHOD_TLSv1_3_SERVER`**(починаючи з PHP 7.4.0)

Якщо не вказано, буде використано параметр `crypto_method`из SSL контекста потока.

`session_stream`

Використовувати в потоці налаштування з `session_stream`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, **`false`**, если не удалось установить шифрование или , якщо недостатньо даних і ви повинні спробувати ще раз (тільки для неблокуючих сокетів).

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `session_stream` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання** stream\_socket\_enable\_crypto()\*\*\*\*

```php
<?php
$fp = stream_socket_client("tcp://myproto.example.com:31337", $errno, $errstr, 30);
if (!$fp) {
    die("Не могу соединиться: $errstr ($errno)");
}

/* Включить шифрование для этапа входа в систему */
stream_socket_enable_crypto($fp, true, STREAM_CRYPTO_METHOD_SSLv23_CLIENT);
fwrite($fp, "USER бог\r\n");
fwrite($fp, "PASS секрет\r\n");

/* Отключить шифрование для всего остального */
stream_socket_enable_crypto($fp, false);

while ($motd = fgets($fp)) {
    echo $motd;
}

fclose($fp);
?>
```

Висновок наведеного прикладу буде схожим на:

### Дивіться також

-   [Функції OpenSSL](ref.openssl.md)
-   [Список підтримуваних транспортних протоколів](transports.md)
