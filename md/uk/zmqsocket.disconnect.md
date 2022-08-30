Вимкнути сокет

-   [« ZMQSocket::construct](zmqsocket.construct.html)
    
-   [ZMQSocket::getEndpoints »](zmqsocket.getendpoints.html)
    
-   [PHP Manual](index.html)
    
-   [ZMQSocket](class.zmqsocket.html)
    
-   Вимкнути сокет
    

# ZMQSocket::disconnect

(PECL zmq >= 1.0.4)

ZMQSocket::disconnect — Вимкнути сокет

### Опис

```methodsynopsis
public ZMQSocket::disconnect(string $dsn): ZMQSocket
```

Видалити раніше створене з'єднання сокета з кінцевою точкою. Кінцева точка визначається у форматі `transport://address`де транспорт може бути одним з наступних значень: inproc, ipc, tcp, pgm або epgm.

### Список параметрів

`dsn`

Кінцева точка, наприклад `transport://address`

### Значення, що повертаються

Повертає поточний об'єкт. У разі помилки викидає виняток ZMQSocketException.