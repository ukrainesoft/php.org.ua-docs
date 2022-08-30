Клас ZMQContext

-   [« ZMQ::construct](zmq.construct.html)
    
-   [ZMQContext::construct »](zmqcontext.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Обмін повідомленнями 0MQ](book.zmq.html)
    
-   Клас ZMQContext
    

# Клас ZMQContext

(PECL zmq >= 0.5.0)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class ZMQContext
     
     {
    

    /* Методы */
    
   public __construct(int $io_threads = 1, bool $is_persistent = true)
public getOpt(string $key): mixed
public getSocket(int $type, string $persistent_id = null, callable $on_new_socket = null): ZMQSocket
public isPersistent(): bool
public setOpt(int $key, mixed $value): ZMQContext

   }
```

## Зміст

-   [ZMQContext::construct](zmqcontext.construct.html) - Конструктор ZMQContext
-   [ZMQContext::getOpt](zmqcontext.getopt.html) — Отримати опцію контексту
-   [ZMQContext::getSocket](zmqcontext.getsocket.html) - Створює новий сокет
-   [ZMQContext::isPersistent](zmqcontext.ispersistent.html) — Чи контекст є постійним
-   [ZMQContext::setOpt](zmqcontext.setopt.html) - Встановити опцію сокету