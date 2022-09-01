---
navigation:
  - class.zmqpoll.html: « ZMQPoll
  - zmqpoll.clear.html: 'ZMQPoll::clear »'
  - index.html: PHP Manual
  - class.zmqpoll.html: ZMQPoll
title: 'ZMQPoll::add'
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

Визначає, яка активність відстежуватиметься. Дивіться константи **`ZMQ::POLL_IN`** і **`ZMQ::POLL_OUT`**

### Значення, що повертаються

Повертає рядковий ідентифікатор доданого елемента, який можна буде використовувати для його видалення. У разі помилки викидає виняток ZMQPollException.
