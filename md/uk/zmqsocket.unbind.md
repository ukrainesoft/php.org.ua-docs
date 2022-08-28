Відв'язати сокет

-   [« ZMQSocket::setSockOpt](zmqsocket.setsockopt.html)
    
-   [ZMQPoll »](class.zmqpoll.html)
    
-   [PHP Manual](index.html)
    
-   [ZMQSocket](class.zmqsocket.html)
    
-   Відв'язати сокет
    

# ZMQSocket::unbind

(PECL zmq >= 1.0.4)

ZMQSocket::unbind — Відв'язати сокет

### Опис

```methodsynopsis
public ZMQSocket::unbind(string $dsn): ZMQSocket
```

Відв'язує сокет від кінцевої точки. Кінцева точка визначається у форматі `transport://address`де транспорт може бути одним з наступних значень: inproc, ipc, tcp, pgm або epgm.

### Список параметрів

`dsn`

Попередньо прив'язана кінцева точка, наприклад `transport://address`

### Значення, що повертаються

Повертає поточний об'єкт. У разі помилки викидає виняток ZMQSocketException.