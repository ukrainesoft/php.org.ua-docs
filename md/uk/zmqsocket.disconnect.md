---
navigation:
  - zmqsocket.construct.md: '« ZMQSocket::\_\_construct'
  - zmqsocket.getendpoints.md: 'ZMQSocket::getEndpoints »'
  - index.md: PHP Manual
  - class.zmqsocket.md: ZMQSocket
title: 'ZMQSocket::disconnect'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZMQSocket::disconnect

(PECL zmq >= 1.0.4)

ZMQSocket::disconnect — Вимкнути сокет

### Опис

```methodsynopsis
public ZMQSocket::disconnect(string $dsn): ZMQSocket
```

Видалити раніше створене з'єднання сокета з кінцевою точкою. Кінцева точка визначається у форматі `transport://address`де транспорт може бути одним з наступних значень: inproc, ipc, tcp, pgm або epgm.

### Список параметрів

`dsn`

Кінцева точка, наприклад `transport://address`

### Значення, що повертаються

Повертає поточний об'єкт. У разі помилки викидає виняток ZMQSocketException.
