---
navigation:
  - zmqsocket.sendmulti.md: '« ZMQSocket::sendmulti'
  - zmqsocket.unbind.md: 'ZMQSocket::unbind »'
  - index.md: PHP Manual
  - class.zmqsocket.md: ZMQSocket
title: 'ZMQSocket::setSockOpt'
---
# ZMQSocket::setSockOpt

(PECL zmq >= 0.5.0)

ZMQSocket::setSockOpt — Встановити опцію сокету

### Опис

```methodsynopsis
public ZMQSocket::setSockOpt(int $key, mixed $value): ZMQSocket
```

Встановлює опцію сокету ZMQ. Тип параметра `value` залежить від значення параметра `key`. Дивіться [Типи констант ZMQ](class.zmq.md#zmq.constants)

### Список параметрів

`key`

Одна з констант **`ZMQ::SOCKOPT_*`**

`value`

Значення, що встановлюється.

### Значення, що повертаються

Повертає поточний об'єкт. У разі помилки викидає виняток ZMQSocketException.
