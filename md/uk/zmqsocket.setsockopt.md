---
navigation:
  - zmqsocket.sendmulti.md: '« ZMQSocket::sendmulti'
  - zmqsocket.unbind.md: 'ZMQSocket::unbind »'
  - index.md: PHP Manual
  - class.zmqsocket.md: ZMQSocket
title: 'ZMQSocket::setSockOpt'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZMQSocket::setSockOpt

(PECL zmq >= 0.5.0)

ZMQSocket::setSockOpt — Встановити опцію сокету

### Опис

```methodsynopsis
public ZMQSocket::setSockOpt(int $key, mixed $value): ZMQSocket
```

Устанавливает опцию сокета ZMQ. Тип параметра`value`зависит от значения параметра`key`Смотрите[Типи констант ZMQ](class.zmq.md#zmq.constants)

### Список параметрів

`key`

Одна из констант\*\*`ZMQ::SOCKOPT_*`\*\*

`value`

Значення, що встановлюється.

### Значення, що повертаються

Повертає поточний об'єкт. У разі помилки викидає виняток ZMQSocketException.
