---
navigation:
  - zmqpoll.count.md: '« ZMQPoll::count'
  - zmqpoll.poll.md: 'ZMQPoll::poll »'
  - index.md: PHP Manual
  - class.zmqpoll.md: ZMQPoll
title: 'ZMQPoll::getLastErrors'
---
# ZMQPoll::getLastErrors

(PECL zmq >= 0.5.0)

ZMQPoll::getLastErrors — Повертає помилки останнього опитування

### Опис

```methodsynopsis
public ZMQPoll::getLastErrors(): array
```

Повертає ідентифікатори елементів, для яких під час останнього опитування виникли помилки.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив з ідентифікаторами елементів пулу опитування, для яких при останньому опитуванні виникли помилки. Порожній масив означає, що помилок був.
