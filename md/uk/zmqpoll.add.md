---
navigation:
  - class.zmqpoll.md: « ZMQPoll
  - zmqpoll.clear.md: 'ZMQPoll::clear »'
  - index.md: PHP Manual
  - class.zmqpoll.md: ZMQPoll
title: 'ZMQPoll::add'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZMQPoll::add

(PECL zmq >= 0.5.0)

ZMQPoll::add — Додати елемент у пул опитування

### Опис

```methodsynopsis
public ZMQPoll::add(mixed $entry, int $type): string
```

Додає елемент у пул опитування та повертає його внутрішній ідентифікатор у вигляді рядка. Надалі, за цим ідентифікатором, елемент можна видалити.

### Список параметрів

`entry`

Об'єкт ZMQSocket або потоковий ресурс PHP

`type`

Визначає, яка активність відстежуватиметься. Дивіться константи **`ZMQ::POLL_IN`**и**`ZMQ::POLL_OUT`**

### Значення, що повертаються

Повертає рядковий ідентифікатор доданого елемента, який можна буде використовувати для його видалення. У разі помилки викидає виняток ZMQPollException.
