Чи є контекст постійним

-   [« ZMQContext::getSocket](zmqcontext.getsocket.html)
    
-   [ZMQContext::setOpt »](zmqcontext.setopt.html)
    
-   [PHP Manual](index.html)
    
-   [ZMQContext](class.zmqcontext.html)
    
-   Чи є контекст постійним
    

# ZMQContext::isPersistent

(PECL zmq >= 0.5.0)

ZMQContext::isPersistent — Чи є контекст постійним

### Опис

```methodsynopsis
public ZMQContext::isPersistent(): bool
```

Визначає, чи контекст є постійним. Постійний контекст потрібний для постійного з'єднання, оскільки кожен сокет виділяється з контексту.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо контекст постійний і **`false`**, якщо ні.