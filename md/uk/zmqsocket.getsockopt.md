Отримати опцію сокету

-   [« ZMQSocket::getSocketType](zmqsocket.getsockettype.html)
    
-   [ZMQSocket::isPersistent »](zmqsocket.ispersistent.html)
    
-   [PHP Manual](index.html)
    
-   [ZMQSocket](class.zmqsocket.html)
    
-   Отримати опцію сокету
    

# ZMQSocket::getSockOpt

(PECL zmq >= 0.5.0)

ZMQSocket::getSockOpt — Отримати опцію сокету

### Опис

```methodsynopsis
public ZMQSocket::getSockOpt(string $key): mixed
```

Повертає значення опції сокету.

### Список параметрів

`key`

Ціле число, яке представляє опцію сокету. Дивіться константи **`ZMQ::SOCKOPT_*`**

### Значення, що повертаються

Повертає string або int, залежно від значення параметра `key`. У разі помилки викидає виняток ZMQSocketException.