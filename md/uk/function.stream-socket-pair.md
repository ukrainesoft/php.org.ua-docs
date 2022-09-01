---
navigation:
  - function.stream-socket-get-name.html: « streamsocketgetname
  - function.stream-socket-recvfrom.html: streamsocketrecvfrom »
  - index.html: PHP Manual
  - ref.stream.html: Функції для роботи з потоками
title: streamsocketpair
---
# streamsocketpair

(PHP 5> = 5.1.0, PHP 7, PHP 8)

streamsocketpair — Створює пару підключених, невиразних потоків сокетів

### Опис

```methodsynopsis
stream_socket_pair(int $domain, int $type, int $protocol): array|false
```

**streamsocketpair()** створює пару підключених, невиразних потоків сокетів. Ця функція зазвичай використовується в IPC (міжпроцесної взаємодії).

### Список параметрів

`domain`

Використовуване сімейство протоколів: **`STREAM_PF_INET`** **`STREAM_PF_INET6`** або **`STREAM_PF_UNIX`**

`type`

Тип взаємодії, що використовується: **`STREAM_SOCK_DGRAM`** **`STREAM_SOCK_RAW`** **`STREAM_SOCK_RDM`** **`STREAM_SOCK_SEQPACKET`** або **`STREAM_SOCK_STREAM`**

`protocol`

Використовуваний протокол: **`STREAM_IPPROTO_ICMP`** **`STREAM_IPPROTO_IP`** **`STREAM_IPPROTO_RAW`** **`STREAM_IPPROTO_TCP`** ор **`STREAM_IPPROTO_UDP`**

> **Зауваження**: Будь ласка, зверніться до розділу [Список потокових констант](stream.constants.html) за детальною інформацією щодо кожної константи.

### Значення, що повертаються

Повертає масив (array) з двома потоковими ресурсами у разі успішного виконання, або **`false`** у разі невдачі.

### Приклади

**Приклад #1 Приклад використання **streamsocketpair()****

Цей приклад демонструє основи використання функції **streamsocketpair()** у міжпроцесній взаємодії.

```php
<?php

$sockets = stream_socket_pair(STREAM_PF_UNIX, STREAM_SOCK_STREAM, STREAM_IPPROTO_IP);
$pid     = pcntl_fork();

if ($pid == -1) {
     die('не удалось создать процесс');

} else if ($pid) {
     /* родительский процесс */
    fclose($sockets[0]);

    fwrite($sockets[1], "дочерний PID: $pid\n");
    echo fgets($sockets[1]);

    fclose($sockets[1]);

} else {
    /* дочерний процесс */
    fclose($sockets[1]);

    fwrite($sockets[0], "сообщение от дочернего процесса\n");
    echo fgets($sockets[0]);

    fclose($sockets[0]);
}

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
дочерний PID: 1378
сообщение от дочернего процесса
```
