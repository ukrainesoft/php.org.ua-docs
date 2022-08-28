Встановити опцію сокету

-   [« ZMQSocket::sendmulti](zmqsocket.sendmulti.html)
    
-   [ZMQSocket::unbind »](zmqsocket.unbind.html)
    
-   [PHP Manual](index.html)
    
-   [ZMQSocket](class.zmqsocket.html)
    
-   Встановити опцію сокету
    

# ZMQSocket::setSockOpt

(PECL zmq >= 0.5.0)

ZMQSocket::setSockOpt — Встановити опцію сокету

### Опис

```methodsynopsis
public ZMQSocket::setSockOpt(int $key, mixed $value): ZMQSocket
```

Встановлює опцію сокету ZMQ. Тип параметра `value` залежить від значення параметра `key`. Дивіться [Типы констант ZMQ](class.zmq.html#zmq.constants)

### Список параметрів

`key`

Одна з констант **`ZMQ::SOCKOPT_*`**

`value`

Значення, що встановлюється.

### Значення, що повертаються

Повертає поточний об'єкт. У разі помилки викидає виняток ZMQSocketException.