---
navigation:
  - function.stream-socket-server.md: « streamsocketserver
  - function.stream-supports-lock.md: streamsupportslock »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: streamsocketshutdown
---
# streamsocketshutdown

(PHP 5> = 5.2.1, PHP 7, PHP 8)

streamsocketshutdown — Закрити повнодуплексне з'єднання

### Опис

```methodsynopsis
stream_socket_shutdown(resource $stream, int $mode): bool
```

Закриває (частково чи ні) повнодуплексне з'єднання.

> **Зауваження**
> 
> Асоційовані буфери або буфери можуть бути закриті, а можуть і ні.

### Список параметрів

`stream`

Відкритий потік (наприклад, відкритий за допомогою функції [streamsocketclient()](function.stream-socket-client.md)

`mode`

Одна з наступних констант: **`STREAM_SHUT_RD`** (відключає подальше отримання даних), **`STREAM_SHUT_WR`** (відключає подальшу передачу даних) або **`STREAM_SHUT_RDWR`** (Вимикає подальше отримання та передачу даних).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **streamsocketshutdown()****

```php
<?php

$server = stream_socket_server('tcp://127.0.0.1:1337');
$client = stream_socket_client('tcp://127.0.0.1:1337');

var_dump(fputs($client, "привет"));

stream_socket_shutdown($client, STREAM_SHUT_WR);
var_dump(fputs($client, "привет")); // не работает сейчас

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(5)

Notice: fputs(): send of 6 bytes failed with errno=32 Broken pipe in test.php on line 9
int(0)
```

### Дивіться також

-   [fclose()](function.fclose.md) - Закриває відкритий дескриптор файлу
