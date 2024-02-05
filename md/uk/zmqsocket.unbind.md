---
navigation:
  - zmqsocket.setsockopt.md: '« ZMQSocket::setSockOpt'
  - class.zmqpoll.md: ZMQPoll »
  - index.md: PHP Manual
  - class.zmqsocket.md: ZMQSocket
title: 'ZMQSocket::unbind'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZMQSocket::unbind

(PECL zmq >= 1.0.4)

ZMQSocket::unbind — Відв'язати сокет

### Опис

```methodsynopsis
public ZMQSocket::unbind(string $dsn): ZMQSocket
```

Відв'язує сокет від кінцевої точки. Кінцева точка визначається у форматі `transport://address`де транспорт може бути одним з наступних значень: inproc, ipc, tcp, pgm або epgm.

### Список параметрів

`dsn`

Попередньо прив'язана кінцева точка, наприклад `transport://address`

### Значення, що повертаються

Повертає поточний об'єкт. У разі помилки викидає виняток ZMQSocketException.
