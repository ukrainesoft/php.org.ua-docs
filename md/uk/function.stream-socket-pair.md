---
navigation:
  - function.stream-socket-get-name.md: « stream\_socket\_get\_name
  - function.stream-socket-recvfrom.md: stream\_socket\_recvfrom »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_socket\_pair
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_socket\_pair

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

stream\_socket\_pair — Створює пару підключених, невиразних потоків сокетів

### Опис

```methodsynopsis
stream_socket_pair(int $domain, int $type, int $protocol): array|false
```

**stream\_socket\_pair()** створює пару підключених, невиразних потоків сокетів. Ця функція зазвичай використовується в IPC (міжпроцесної взаємодії).

### Список параметрів

`domain`

Используемое семейство протоколов:**`STREAM_PF_INET`** **`STREAM_PF_INET6`** або **`STREAM_PF_UNIX`**

`type`

Тип взаємодії, що використовується: **`STREAM_SOCK_DGRAM`** **`STREAM_SOCK_RAW`** **`STREAM_SOCK_RDM`** **`STREAM_SOCK_SEQPACKET`** або **`STREAM_SOCK_STREAM`**

`protocol`

Використовуваний протокол: **`STREAM_IPPROTO_ICMP`** **`STREAM_IPPROTO_IP`** **`STREAM_IPPROTO_RAW`** **`STREAM_IPPROTO_TCP`**or**`STREAM_IPPROTO_UDP`**

> **Зауваження**: Пожалуйста, обратитесь к разделу[Список потокових констант](stream.constants.md)за подробной информацией по каждой константе.

### Значення, що повертаються

Повертає масив (array) з двома потоковими ресурсами у разі успішного виконання, або \*\*`false`\*\*в случае неудачи.

### Приклади

**Приклад #1 Приклад використання** stream\_socket\_pair()\*\*\*\*

Цей приклад демонструє основи використання функції **stream\_socket\_pair()** у міжпроцесній взаємодії.

```php
<?php

$sockets = stream_socket_pair(STREAM_PF_UNIX, STREAM_SOCK_STREAM, STREAM_IPPROTO_IP);
$pid     = pcntl_fork();

if ($pid == -1) {
     die('не удалось создать процесс');

} else if ($pid) {
     /* родительский процесс */
    fclose($sockets[0]);

    fwrite($sockets[1], "дочерний PID: $pid\n");
    echo fgets($sockets[1]);

    fclose($sockets[1]);

} else {
    /* дочерний процесс */
    fclose($sockets[1]);

    fwrite($sockets[0], "сообщение от дочернего процесса\n");
    echo fgets($sockets[0]);

    fclose($sockets[0]);
}

?>
```

Висновок наведеного прикладу буде схожим на:

```
дочерний PID: 1378
сообщение от дочернего процесса
```
