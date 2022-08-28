Прив'язка сокету

-   [« ZMQSocket](class.zmqsocket.html)
    
-   [ZMQSocket::connect »](zmqsocket.connect.html)
    
-   [PHP Manual](index.html)
    
-   [ZMQSocket](class.zmqsocket.html)
    
-   Прив'язка сокету
    

# ZMQSocket::bind

(PECL zmq >= 0.5.0)

ZMQSocket::bind — Прив'язка сокету

### Опис

```methodsynopsis
public ZMQSocket::bind(string $dsn, bool $force = false): ZMQSocket
```

Прив'язка сокета до кінцевої точки. Кінцева точка визначається у форматі `transport://address`. Як транспорт можуть використовуватися такі протоколи: inproc, ipc, tcp, pgm або epgm

### Список параметрів

`dsn`

Кінцева точка, наприклад `transport://address`

`force`

Вказує, чи намагатиметься підключитися, якщо підключення до вказаної точки вже було встановлено.

### Значення, що повертаються

Повертає поточний об'єкт. У разі помилки викидає виняток ZMQSocketException.