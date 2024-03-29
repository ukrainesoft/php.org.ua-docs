---
navigation:
  - zmqsocket.recv.md: '« ZMQSocket::recv'
  - zmqsocket.send.md: 'ZMQSocket::send »'
  - index.md: PHP Manual
  - class.zmqsocket.md: ZMQSocket
title: 'ZMQSocket::recvMulti'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZMQSocket::recvMulti

(PECL zmq >= 0.8.0)

ZMQSocket::recvMulti — Отримати повідомлення, що складається з кількох частин

### Опис

```methodsynopsis
public ZMQSocket::recvMulti(int $mode = 0): array
```

Отримує масив із повідомленням із сокету. За промовчанням отримання буде блокуватися доти, доки повідомлення не буде доступне, тільки якщо не встановлено прапорець **`ZMQ::MODE_NOBLOCK`**

### Список параметрів

`mode`

Прапори для налаштування режиму, що не блокує отримання та роботи з повідомленнями, що складаються з декількох частин. Дивіться константи **`ZMQ::MODE_*`**

### Значення, що повертаються

Повертає масив із частинами повідомлення. У разі помилки викидає виняток ZMQSocketException. Якщо використовується режим **`ZMQ::MODE_NOBLOCK`** і операцію заблоковано, то буде повернуто **`false`**
