---
navigation:
  - zmqsocket.getpersistentid.md: '« ZMQSocket::getPersistentId'
  - zmqsocket.getsockopt.md: 'ZMQSocket::getSockOpt »'
  - index.md: PHP Manual
  - class.zmqsocket.md: ZMQSocket
title: 'ZMQSocket::getSocketType'
---
# ZMQSocket::getSocketType

(PECL zmq >= 0.5.0)

ZMQSocket::getSocketType — Отримати тип сокету

### Опис

```methodsynopsis
public ZMQSocket::getSocketType(): int
```

Повертає тип сокету.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ціле уявлення типу сокета. Це значення співвідноситься з однією з констант **`ZMQ::SOCKET_*`**
