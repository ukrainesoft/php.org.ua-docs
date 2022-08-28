Надіслати повідомлення

-   [« ZMQSocket::recvMulti](zmqsocket.recvmulti.html)
    
-   [ZMQSocket::sendmulti »](zmqsocket.sendmulti.html)
    
-   [PHP Manual](index.html)
    
-   [ZMQSocket](class.zmqsocket.html)
    
-   Надіслати повідомлення
    

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