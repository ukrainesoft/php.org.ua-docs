---
navigation:
  - zmqsocket.ispersistent.md: '« ZMQSocket::isPersistent'
  - zmqsocket.recvmulti.md: 'ZMQSocket::recvMulti »'
  - index.md: PHP Manual
  - class.zmqsocket.md: ZMQSocket
title: 'ZMQSocket::recv'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZMQSocket::recv

(PECL zmq >= 0.5.0)

ZMQSocket::recv — Отримати повідомлення

### Опис

```methodsynopsis
public ZMQSocket::recv(int $mode = 0): string
```

Отримує повідомлення із сокету. За промовчанням отримання буде блокуватися доти, доки повідомлення не буде доступне, тільки якщо не встановлено прапорець **`ZMQ::MODE_DONTWAIT`**. Можна використовувати опцію сокету **`ZMQ::SOCKOPT_RCVMORE`** для отримання повідомлень, що складаються з декількох частин. Детальніше дивіться [ZMQSocket::setSockOpt()](zmqsocket.setsockopt.md)

### Список параметрів

`mode`

Прапори для налаштування режиму, що не блокує отримання та роботи з повідомленнями, що складаються з декількох частин. Дивіться константи **`ZMQ::MODE_*`**

### Значення, що повертаються

Повертає повідомлення. Якщо використовується режим **`ZMQ::MODE_DONTWAIT`** і операцію заблоковано, то буде повернуто **`false`**

### Помилки

Викидає **ZMQSocketException**в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад надсилання/отримання**

Чи не блокує відправка/отримання

```php
<?php

/* Создаём новый объект очереди. Необходим сервер на другой стороне. */
$queue = new ZMQSocket(new ZMQContext(), ZMQ::SOCKET_REQ);
$queue->connect("tcp://127.0.0.1:5555");

/* Привязываем сокет 1 к очереди, отправляем и получаем */
$retries = 5;
$sending = true;

/* Запускаем цикл */
do {
    try {
        /* Пытаемся отправить/получить */
        if ($sending) {
            echo "Отправляем сообщение\n";
            $queue->send("Я сообщение!", ZMQ::MODE_DONTWAIT);
            $sending = false;
        } else {
            echo "Получен ответ: " . $queue->recv(ZMQ::MODE_DONTWAIT) . "\n";
            break;
        }
    } catch (ZMQSocketException $e) {
        /* EAGAIN означает, что операция заблокирована, повторяем */
        if ($e->getCode() === ZMQ::ERR_EAGAIN) {
            echo " - Получили EAGAIN, повторяем ($retries)\n";
        } else {
            die(" - Ошибка: " . $e->getMessage());
        }
    }
    /* Немножко ждём */
    usleep(5);
} while (--$retries);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Отправляем сообщение
 - Получили EAGAIN, повторяем (4)
Получен ответ: Я сообщение!
```
