---
navigation:
  - migration56.new-functions.md: « Нові функції
  - migration56.extensions.md: Інші зміни у модулях »
  - index.md: PHP Manual
  - migration56.md: Міграція з PHP 5.5.x на PHP 5.6.x
title: Зміни OpenSSL у PHP 5.6.x
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Зміни OpenSSL у PHP 5.6.x

### Обгортки потоків тепер за промовчанням перевіряють сертифікати вузлів та імена хостів під час використання SSL/TLS

Всі клієнтські потоки, що шифруються, тепер за замовчуванням включають перевірку бенкетів. За замовчуванням сертифікат бенкету перевіряється пакетом OpenSSL CA. Зазвичай нічого не потрібно робити для з'єднання з серверами з правильним SSL-сертифікатом, оскільки OpenSSL налаштований так, що вже працює з хорошими CA-пакетами.

Стандартний CA пакет може бути перевизначений глобально за допомогою установки або openssl.cafile або openssl.capath рядків конфігурації, або ж на рівні кожного запиту, використовуючи опції контексту [`cafile`](context.ssl.md#context.ssl.cafile) або [`capath`](context.ssl.md#context.ssl.capath)

Хоча це і не рекомендується, але можна вимкнути перевірку сертифіката бенкету для запиту, встановивши [`verify_peer`](context.ssl.md#context.ssl.verify-peer)опцию контекста в\*\*`false`**, і можна вимкнути перевірку імені бенкету, встановивши [`verify_peer_name`](context.ssl.md#context.ssl.verify-peer-name)в**`false`\*\*

### Сигнатура сертифіката

Було додано підтримку вилучення та перевірки сигнатури сертифіката. Для отримання сигнатур сертифікатів X.509 додано функцію [openssl\_x509\_fingerprint()](function.openssl-x509-fingerprint.md). Також було додано дві опції [контексту потоку SSL](context.ssl.md) `capture_peer_cert`для захвата узлового сертификата X.509, и`peer_fingerprint`для проверки сертификата на соответствие заданной сигнатуре.

### Оновлено шифри за замовчуванням

Список стандартних шифрів, що використовуються PHP, був оновлений на більш безпечний відповідно до [»  рекомендаціями щодо шифрів від Mozilla](https://wiki.mozilla.org/Security/Server_Side_TLS#Recommended_Ciphersuite), з двома додатковими винятками: анонімні шифри Діффі-Хеллмана та RC4.

Цей список доступний через нову константу **`OPENSSL_DEFAULT_STREAM_CIPHERS`**, і може бути перевизначений (як і в попередніх версіях PHP) установкою опцією контексту [`ciphers`](context.ssl.md#context.ssl.ciphers)

### Стиснення заборонено за умовчанням

Стиснення SSL/TLS було заборонено за замовчуванням для зменшення зменшення ймовірності атаки типу CRIME. У PHP 5.4.13 було додано опцію контексту [`disable_compression`](context.ssl.md#context.ssl.disable-compression) для можливості заборонити компресію і тепер вона за умовчанням встановлена ​​як **`true`** (тобто компресію заборонено).

### Дозвіл серверу визначати свій власний порядок шифрів

Додано опцію контексту `honor_cipher_order`, яка дозволяє серверу, що обслуговує зашифрований потік, самому визначати шифри, якими буде користуватися клієнт. Це дозволить знизити ризик атаки типу BEAST.

### Доступ до узгодженого протоколу та шифру

Протокол та шифр, узгоджені для шифрованого потоку, доступні за допомогою функцій [stream\_get\_meta\_data()](function.stream-get-meta-data.md) або [stream\_context\_get\_options()](function.stream-context-get-options.md), если опция контекста SSL`capture_session_meta`установлена как\*\*`true`\*\*

```php
<?php
$ctx = stream_context_create(['ssl' => [
    'capture_session_meta' => TRUE
]]);

$html = file_get_contents('https://google.com/', FALSE, $ctx);
$meta = stream_context_get_options($ctx)['ssl']['session_meta'];
var_dump($meta);
?>
```

Результат виконання наведеного прикладу:

```
array(4) {
  ["protocol"]=>
  string(5) "TLSv1"
  ["cipher_name"]=>
  string(20) "ECDHE-RSA-AES128-SHA"
  ["cipher_bits"]=>
  int(128)
  ["cipher_version"]=>
  string(11) "TLSv1/SSLv3"
}
```

### Нові можливості для досконалої прямої секретності (PFS) для серверів, які обслуговують шифровані потоки

Шифровані потоки клієнта вже підтримують пряму таємність, оскільки вона, як правило, контролюється сервером. Сервери PHP, що обслуговують шифровані потоки, використовують сертифікати підтримують досконалу пряму секретність не потребують будь-яких додаткових дій для включення PFS; однак, було додано кілька нових опцій контексту SSL для більш точного контролю над PFS та для вирішення можливих проблем.

`ecdh_curve`

Ця опція дозволяє вибрати криву для використання у шифрах ECDH. Якщо не задано, то використовуватиметься `prime256v1`

`dh_param`

Шлях до файлу, що містить параметри для обміну ключами Діффі-Хеллмана, створеного, наприклад, за допомогою такої команди:

openssl dhparam -out /path/to/my/certs/dh-2048.pem 2048

`single_dh_use`

Если установлено как\*\*`true`\*\*, нова пара ключів буде створена, використовуючи параметри Діффі-Хеллмана, тим самим покращуючи пряму таємність.

`single_ecdh_use`

Если установлено как\*\*`true`\*\*, нова пара ключів буде генеруватися завжди, за узгодженням шифру ECDH. Це покращує пряму таємність.

### Вибір версії SSL/TLS

Тепер можна вибирати конкретну версію SSL та TLS за допомогою опції контексту `crypto_method` або вказуючи конкретний транспорт під час створення обгортки потоку (наприклад, за допомогою виклику [stream\_socket\_client()](function.stream-socket-client.md) або [stream\_socket\_server()](function.stream-socket-server.md)

Опция контекста SSL`crypto_method` приймає бітову маску, що перераховує допустимі протоколи, як і задається в параметрі `crypto_type` функції [stream\_socket\_enable\_crypto()](function.stream-socket-enable-crypto.md)

**Вибрана версія протоколу та відповідні опції**

| Протокол | Флаг клиента | Флаг сервера | Транспорт |
| --- | --- | --- | --- |
| Будь-які версії TLS або SSL | **`STREAM_CRYPTO_METHOD_ANY_CLIENT`** | **`STREAM_CRYPTO_METHOD_ANY_SERVER`** | `ssl://` |
| Будь-яка версія TLS | **`STREAM_CRYPTO_METHOD_TLS_CLIENT`** | **`STREAM_CRYPTO_METHOD_TLS_SERVER`** | `tls://` |
| TLS 1.0 | **`STREAM_CRYPTO_METHOD_TLSv1_0_CLIENT`** | **`STREAM_CRYPTO_METHOD_TLSv1_0_SERVER`** | `tlsv1.0://` |
| TLS 1.1 | **`STREAM_CRYPTO_METHOD_TLSv1_1_CLIENT`** | **`STREAM_CRYPTO_METHOD_TLSv1_1_SERVER`** | `tlsv1.1://` |
| TLS 1.2 | **`STREAM_CRYPTO_METHOD_TLSv1_2_CLIENT`** | **`STREAM_CRYPTO_METHOD_TLSv1_2_SERVER`** | `tlsv1.2://` |
| SSL 3 | **`STREAM_CRYPTO_METHOD_SSLv3_CLIENT`** | **`STREAM_CRYPTO_METHOD_SSLv3_SERVER`** | `sslv3://` |

```php
<?php

// Требуется TLS 1.0 или выше для использования file_get_contents():
$ctx = stream_context_create([
    'ssl' => [
        'crypto_method' => STREAM_CRYPTO_METHOD_TLS_CLIENT,
    ],
]);
$html = file_get_contents('https://google.com/', false, $ctx);

// Требуется TLS 1.1 или 1.2:
$ctx = stream_context_create([
    'ssl' => [
        'crypto_method' => STREAM_CRYPTO_METHOD_TLSv1_1_CLIENT |
                           STREAM_CRYPTO_METHOD_TLSv1_2_CLIENT,
    ],
]);
$html = file_get_contents('https://google.com/', false, $ctx);

// Соединяемся с использованием транспорта потокового сокета tlsv1.2://
$sock = stream_socket_client('tlsv1.2://google.com:443/');

?>
```

### Добавлена функция[openssl\_get\_cert\_locations()](function.openssl-get-cert-locations.md)

Була додана функція [openssl\_get\_cert\_locations()](function.openssl-get-cert-locations.md): вона повертає розташування, в яких PHP шукатиме пакети CA за замовчуванням.

```php
<?php
var_dump(openssl_get_cert_locations());
?>
```

Результат виконання наведеного прикладу:

```
array(8) {
  ["default_cert_file"]=>
  string(21) "/etc/pki/tls/cert.pem"
  ["default_cert_file_env"]=>
  string(13) "SSL_CERT_FILE"
  ["default_cert_dir"]=>
  string(18) "/etc/pki/tls/certs"
  ["default_cert_dir_env"]=>
  string(12) "SSL_CERT_DIR"
  ["default_private_dir"]=>
  string(20) "/etc/pki/tls/private"
  ["default_default_cert_area"]=>
  string(12) "/etc/pki/tls"
  ["ini_cafile"]=>
  string(0) ""
  ["ini_capath"]=>
  string(0) ""
}
```

### Підтримка SPKI

Було додано підтримку для створення, вилучення та перевірки підписаних публічних ключів та розпізнавальних рядків (SPKAC). Були додані функції [openssl\_spki\_new()](function.openssl-spki-new.md) [openssl\_spki\_verify()](function.openssl-spki-verify.md) [openssl\_spki\_export\_challenge()](function.openssl-spki-export-challenge.md) і [openssl\_spki\_export()](function.openssl-spki-export.md) для створення, перевірки експорту PEM публічних ключів та відповідних розпізнавальних рядків із SPKAC, створених з елементів HTML5 `KeyGen`

`openssl_spki_new`

Генерація нового SPKAC з використанням приватного ключа, розпізнавального рядка та алгоритму хешування.

```php
<?php
$pkey = openssl_pkey_new();
openssl_pkey_export($pkey, 'secret passphrase');

$spkac = openssl_spki_new($pkey, 'challenge string');
?>
```

Результат виконання наведеного прикладу:

```
SPKAC=MIIBXjCByDCBnzANBgkqhkiG9w0BAQEFAAOBjQAwgYkCgYEA3L0IfUijj7+A8CPC8EmhcdNoe5fUAog7OrBdhn7EkxFButUp40P7+LiYiygYG1TmoI/a5EgsLU3s9twEz3hmgY9mYIqb/rb+SF8qlD/K6KVyUORC7Wlz1Df4L8O3DuRGzx6/+3jIW6cPBpfgH1sVuYS1vDBsP/gMMIxwTsKJ4P0CAwEAARYkYjViMzYxMTktNjY5YS00ZDljLWEyYzctMGZjNGFhMjVlMmE2MA0GCSqGSIb3DQEBAwUAA4GBAF7hu0ifzmjonhAak2FhhBRsKFDzXdKIkrWxVNe8e0bZzMrWOxFM/rqBgeH3/gtOUDRS5Fnzyq425UsTYbjfiKzxGeCYCQJb1KJ2V5Ij/mIJHZr53WYEXHQTNMGR8RPm7IxwVXVSHIgAfXsXZ9IXNbFbcaLRiSTr9/N4U+MXUWL7
```

`openssl_spki_verify`

Перевірка наданого SPKAC.

```php
<?php
$pkey = openssl_pkey_new();
openssl_pkey_export($pkey, 'secret passphrase');

$spkac = openssl_spki_new($pkey, 'challenge string');
var_dump(openssl_spki_verify($spkac));
?>
```

`openssl_spki_export_challenge`

Експорт пов'язаного розпізнавального рядка із наданого SPKAC.

```php
<?php
$pkey = openssl_pkey_new();
openssl_pkey_export($pkey, 'secret passphrase');

$spkac = openssl_spki_new($pkey, 'challenge string');
$challenge = openssl_spki_export_challenge($spkac);
echo $challenge;
?>
```

Результат виконання наведеного прикладу:

```
challenge string
```

`openssl_spki_export`

Експорт публічного ключа (PEM) RSA у форматі SPKAC.

```php
<?php
$pkey = openssl_pkey_new();
openssl_pkey_export($pkey, 'secret passphrase');

$spkac = openssl_spki_new($pkey, 'challenge string');
echo openssl_spki_export($spkac);
?>
```

Результат виконання наведеного прикладу:

```
-----BEGIN PUBLIC KEY-----
MIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQDcvQh9SKOPv4DwI8LwSaFx02h7
l9QCiDs6sF2GfsSTEUG61SnjQ/v4uJiLKBgbVOagj9rkSCwtTez23ATPeGaBj2Zg
ipv+tv5IXyqUP8ropXJQ5ELtbXPUN/gvw7cO5EbPHr/7eMhbpw8Gl+AfWxW5hLW8
MGw/+AwwjHBOwong/QIDAQAB
-----END PUBLIC KEY-----
```
