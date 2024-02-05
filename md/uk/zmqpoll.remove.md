---
navigation:
  - zmqpoll.poll.md: '« ZMQPoll::poll'
  - class.zmqdevice.md: ZMQDevice »
  - index.md: PHP Manual
  - class.zmqpoll.md: ZMQPoll
title: 'ZMQPoll::remove'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZMQPoll::remove

(PECL zmq >= 0.5.0)

ZMQPoll::remove — Видалити елемент із пула опитування

### Опис

```methodsynopsis
public ZMQPoll::remove(mixed $item): bool
```

Видаляє елемент із пулу опитування. Параметр `item` повинен бути об'єктом ZMQSocket, потоковим ресурсом або ідентифікатором, отриманим у результаті виконання методу [ZMQPoll::add()](zmqpoll.add.md)

### Список параметрів

`item`

Об'єкт ZMQSocket, потік PHP або рядковий ідентифікатор елемента.

### Значення, що повертаються

Повертає **`true`**, якщо видалення виконано успішно та **`false`**, якщо елемент не знайдено.
