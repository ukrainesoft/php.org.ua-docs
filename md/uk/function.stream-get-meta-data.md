---
navigation:
  - function.stream-get-line.md: « streamgetline
  - function.stream-get-transports.md: streamgettransports »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: streamgetmetadata
---
# streamgetmetadata

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

streamgetmetadata — Витягує заголовок/метадані з потоків/файлових покажчиків

### Опис

```methodsynopsis
stream_get_meta_data(resource $stream): array
```

Отримує інформацію про існуючий потік `stream`

### Список параметрів

`stream`

Параметр stream може бути будь-яким потоком, створеним за допомогою функцій [fopen()](function.fopen.md) [fsockopen()](function.fsockopen.md) [pfsockopen()](function.pfsockopen.md) і [streamsocketclient()](function.stream-socket-client.md)

### Значення, що повертаються

Отримуваний масив містить такі елементи:

-   `timed_out` (bool) - **`true`**, якщо потік перевищив час очікування даних під час останнього виклику функції [fread()](function.fread.md) або [fgets()](function.fgets.md)
    
-   `blocked` (bool) - \*\*`true`\*\*якщо потік знаходиться в режимі блокуючого введення-виводу. Дивіться функцію [streamsetblocking()](function.stream-set-blocking.md)
    
-   `eof` (bool) - \*\*`true`\*\*якщо потік досяг кінця файлу. Зауважте, що для потоків типу socket цей член може дорівнювати **`true`**, навіть коли `unread_bytes` не дорівнює нулю. Для того, щоб визначити, чи є ще дані для читання, використовуйте [feof()](function.feof.md) замість читання цього елемента.
    
-   `unread_bytes` (int) - кількість байт, що знаходяться зараз у своєму внутрішньому буфері PHP.
    
    > **Зауваження**: Ви не повинні використовувати це значення у скрипті.
    
-   `stream_type` (string) - Мітка, що описує внутрішню реалізацію потоку.
    
-   `wrapper_type` (string) - Мітка, що описує реалізацію обгортки протоколу, накладеного на потік. Дивіться розділ [Підтримувані протоколи та обгортки](wrappers.md) для детальної інформації про обгортки.
    
-   `wrapper_data` (mixed) – специфічні для обгортки дані, прикріплені до цього потоку. Дивіться розділ [Підтримувані протоколи та обгортки](wrappers.md) для детальної інформації про обгортки та їх дані.
    
-   `mode` (string) - тип доступу, необхідний цього потоку (див. таблицю 1 у описі функції [fopen()](function.fopen.md)
    
-   `seekable` (bool) - можна переміщатися по поточному потоку.
    
-   `uri` (string) – URI/ім'я файлу, пов'язане з цим потоком.
    
-   `crypto` (array) – метадані TLS-з'єднання потоку. Примітка: вказується лише в тому випадку, якщо ресурс потоку використовує TLS.
    

### Приклади

**Приклад #1 Приклад використання **streamgetmetadata()** з використанням [fopen()](function.fopen.md) з http**

```php
<?php
$url = 'http://www.example.com/';

if (!$fp = fopen($url, 'r')) {
    trigger_error("Невозможно открыть URL ($url)", E_USER_ERROR);
}

$meta = stream_get_meta_data($fp);

var_dump($meta);

fclose($fp);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(10) {
  'timed_out' =>
  bool(false)
  'blocked' =>
  bool(true)
  'eof' =>
  bool(false)
  'wrapper_data' =>
  array(13) {
    [0] =>
    string(15) "HTTP/1.1 200 OK"
    [1] =>
    string(11) "Age: 244629"
    [2] =>
    string(29) "Cache-Control: max-age=604800"
    [3] =>
    string(38) "Content-Type: text/html; charset=UTF-8"
    [4] =>
    string(35) "Date: Sat, 20 Nov 2021 18:17:57 GMT"
    [5] =>
    string(24) "Etag: "3147526947+ident""
    [6] =>
    string(38) "Expires: Sat, 27 Nov 2021 18:17:57 GMT"
    [7] =>
    string(44) "Last-Modified: Thu, 17 Oct 2019 07:18:26 GMT"
    [8] =>
    string(22) "Server: ECS (chb/0286)"
    [9] =>
    string(21) "Vary: Accept-Encoding"
    [10] =>
    string(12) "X-Cache: HIT"
    [11] =>
    string(20) "Content-Length: 1256"
    [12] =>
    string(17) "Connection: close"
  }
  'wrapper_type' =>
  string(4) "http"
  'stream_type' =>
  string(14) "tcp_socket/ssl"
  'mode' =>
  string(1) "r"
  'unread_bytes' =>
  int(1256)
  'seekable' =>
  bool(false)
  'uri' =>
  string(23) "http://www.example.com/"
}
```

**Приклад #2 Приклад використання **streamgetmetadata()** з використанням [streamsocketclient()](function.stream-socket-client.md) з https**

```php
<?php
$streamContext = stream_context_create(
    [
        'ssl' => [
            'capture_peer_cert' => true,
            'capture_peer_cert_chain' => true,
            'disable_compression' => true,
        ],
    ]
);
$client = stream_socket_client(
    'ssl://www.example.com:443',
    $errorNumber,
    $errorDescription,
    40,
    STREAM_CLIENT_CONNECT,
    $streamContext
);
$meta = stream_get_meta_data($client);
var_dump($meta);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(8) {
  'crypto' =>
  array(4) {
    'protocol' =>
    string(7) "TLSv1.3"
    'cipher_name' =>
    string(22) "TLS_AES_256_GCM_SHA384"
    'cipher_bits' =>
    int(256)
    'cipher_version' =>
    string(7) "TLSv1.3"
  }
  'timed_out' =>
  bool(false)
  'blocked' =>
  bool(true)
  'eof' =>
  bool(false)
  'stream_type' =>
  string(14) "tcp_socket/ssl"
  'mode' =>
  string(2) "r+"
  'unread_bytes' =>
  int(0)
  'seekable' =>
  bool(false)
}
```

### Примітки

> **Зауваження**
> 
> Ця функція НЕ працюватиме з сокетами, створеними за допомогою [модуля Socket](ref.sockets.md)

### Дивіться також

-   [getheaders()](function.get-headers.md) - Повертає всі заголовки з відповіді сервера на запит HTTP
-   [$httpresponseheader](reserved.variables.httpresponseheader.md)
