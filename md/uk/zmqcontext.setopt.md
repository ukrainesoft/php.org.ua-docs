Встановити опцію сокету

-   [« ZMQContext::isPersistent](zmqcontext.ispersistent.html)
    
-   [ZMQSocket »](class.zmqsocket.html)
    
-   [PHP Manual](index.html)
    
-   [ZMQContext](class.zmqcontext.html)
    
-   Встановити опцію сокету
    

# ZMQContext::setOpt

(PECL zmq >= 1.0.4)

ZMQContext::setOpt — Встановити опцію сокету

### Опис

```methodsynopsis
public ZMQContext::setOpt(int $key, mixed $value): ZMQContext
```

Встановлює опцію контексту ZMQ. Тип `value` залежить від `key`. Дивіться [Типы Констант ZMQ](class.zmq.html#zmq.constants)

### Список параметрів

`key`

Одна з констант **`ZMQ::CTXOPT_*`**

`value`

Значення параметру.

### Значення, що повертаються

Повертає поточний об'єкт. У разі помилки викидає виняток ZMQContextException.