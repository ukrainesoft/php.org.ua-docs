---
navigation:
  - zmqsocket.disconnect.md: '« ZMQSocket::disconnect'
  - zmqsocket.getpersistentid.md: 'ZMQSocket::getPersistentId »'
  - index.md: PHP Manual
  - class.zmqsocket.md: ZMQSocket
title: 'ZMQSocket::getEndpoints'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZMQSocket::getEndpoints

(PECL zmq >= 0.5.0)

ZMQSocket::getEndpoints — Отримати список кінцевих точок

### Опис

```methodsynopsis
public ZMQSocket::getEndpoints(): array
```

Повертає список кінцевих точок, з якими з'єднаний або пов'язаний сокет.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив з елементами 'bind' та 'connect'.
