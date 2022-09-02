---
navigation:
  - zmqsocket.recvmulti.md: '« ZMQSocket::recvMulti'
  - zmqsocket.sendmulti.md: 'ZMQSocket::sendmulti »'
  - index.md: PHP Manual
  - class.zmqsocket.md: ZMQSocket
title: 'ZMQSocket::send'
---
# ZMQSocket::send

(PECL zmq >= 0.5.0)

ZMQSocket::send — Надіслати повідомлення

### Опис

```methodsynopsis
public ZMQSocket::send(string $message, int $mode = 0): ZMQSocket
```

Надсилає повідомлення. Операція може блокуватися, якщо не використовується прапор **`ZMQ::MODE_NOBLOCK`**

### Список параметрів

`message`

Повідомлення для надсилання.

`mode`

Прапори для налаштування режиму, що не блокує отримання та роботи з повідомленнями, що складаються з декількох частин. Дивіться константи **`ZMQ::MODE_*`**

### Значення, що повертаються

Повертає поточний об'єкт. У разі помилки викидає виняток ZMQSocketException. Якщо використовується режим **`ZMQ::MODE_NOBLOCK`** і операцію заблоковано, то буде повернуто **`false`**
