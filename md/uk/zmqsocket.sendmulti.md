---
navigation:
  - zmqsocket.send.md: '« ZMQSocket::send'
  - zmqsocket.setsockopt.md: 'ZMQSocket::setSockOpt »'
  - index.md: PHP Manual
  - class.zmqsocket.md: ZMQSocket
title: 'ZMQSocket::sendmulti'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZMQSocket::sendmulti

(PECL zmq >= 0.8.0)

ZMQSocket::sendmulti — Надіслати повідомлення, що складається з кількох частин

### Опис

```methodsynopsis
public ZMQSocket::sendmulti(array $message, int $mode = 0): ZMQSocket
```

Надіслати повідомлення, що складається з декількох частин Операція може блокуватися, якщо прапор не використовується **`ZMQ::MODE_NOBLOCK`**

### Список параметрів

`message`

Повідомлення у вигляді масиву рядків

`mode`

Прапори для налаштування режиму, що не блокує отримання та роботи з повідомленнями, що складаються з декількох частин. Дивіться константи **`ZMQ::MODE_*`**

### Значення, що повертаються

Повертає поточний об'єкт. У разі помилки викидає виняток ZMQSocketException. Якщо використовується режим **`ZMQ::MODE_NOBLOCK`** і операцію заблоковано, то буде повернуто **`false`**
