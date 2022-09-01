---
navigation:
  - zmqsocket.getsockettype.html: '« ZMQSocket::getSocketType'
  - zmqsocket.ispersistent.html: 'ZMQSocket::isPersistent »'
  - index.html: PHP Manual
  - class.zmqsocket.html: ZMQSocket
title: 'ZMQSocket::getSockOpt'
---
# ZMQSocket::getSockOpt

(PECL zmq >= 0.5.0)

ZMQSocket::getSockOpt — Отримати опцію сокету

### Опис

```methodsynopsis
public ZMQSocket::getSockOpt(string $key): mixed
```

Повертає значення опції сокету.

### Список параметрів

`key`

Ціле число, яке представляє опцію сокету. Дивіться константи **`ZMQ::SOCKOPT_*`**

### Значення, що повертаються

Повертає string або int, залежно від значення параметра `key`. У разі помилки викидає виняток ZMQSocketException.
