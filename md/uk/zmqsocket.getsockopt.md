---
navigation:
  - zmqsocket.getsockettype.md: '« ZMQSocket::getSocketType'
  - zmqsocket.ispersistent.md: 'ZMQSocket::isPersistent »'
  - index.md: PHP Manual
  - class.zmqsocket.md: ZMQSocket
title: 'ZMQSocket::getSockOpt'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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
