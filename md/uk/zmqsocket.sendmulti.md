Надіслати повідомлення, що складається з кількох частин

-   [« ZMQSocket::send](zmqsocket.send.html)
    
-   [ZMQSocket::setSockOpt »](zmqsocket.setsockopt.html)
    
-   [PHP Manual](index.html)
    
-   [ZMQSocket](class.zmqsocket.html)
    
-   Надіслати повідомлення, що складається з кількох частин
    

# ZMQSocket::sendmulti

(PECL zmq >= 0.8.0)

ZMQSocket::sendmulti — Надіслати повідомлення, що складається з кількох частин

### Опис

```methodsynopsis
public ZMQSocket::sendmulti(array $message, int $mode = 0): ZMQSocket
```

Надіслати повідомлення, що складається з кількох частин Операція може блокуватися, якщо не використовується прапор **`ZMQ::MODE_NOBLOCK`**

### Список параметрів

`message`

Повідомлення у вигляді масиву рядків

`mode`

Прапори для налаштування режиму, що не блокує отримання та роботи з повідомленнями, що складаються з декількох частин. Дивіться константи **`ZMQ::MODE_*`**

### Значення, що повертаються

Повертає поточний об'єкт. У разі помилки викидає виняток ZMQSocketException. Якщо використовується режим **`ZMQ::MODE_NOBLOCK`** і операцію заблоковано, то буде повернуто **`false`**