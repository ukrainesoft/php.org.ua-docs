Отримати опцію контексту

-   [« ZMQContext::construct](zmqcontext.construct.md)
    
-   [ZMQContext::getSocket »](zmqcontext.getsocket.md)
    
-   [PHP Manual](index.md)
    
-   [ZMQContext](class.zmqcontext.md)
    
-   Отримати опцію контексту
    

# ZMQContext::getOpt

(PECL zmq >= 1.0.4)

ZMQContext::getOpt — Отримати опцію контексту

### Опис

```methodsynopsis
public ZMQContext::getOpt(string $key): mixed
```

Повертає значення опції контексту.

### Список параметрів

`key`

Ціле число, що відображає значення опції. Дивіться опис констант **`ZMQ::CTXOPT_*`**

### Значення, що повертаються

Повертає string або int залежно від `key`. У разі помилки викидає виняток ZMQContextException.