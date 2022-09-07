---
navigation:
  - zmq.construct.md: '« ZMQ::construct'
  - zmqcontext.construct.md: 'ZMQContext::construct »'
  - index.md: PHP Manual
  - book.zmq.md: Обмін повідомленнями 0MQ
title: Клас ZMQContext
---
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

-   [ZMQContext::construct](zmqcontext.construct.md) - Конструктор ZMQContext
-   [ZMQContext::getOpt](zmqcontext.getopt.md) — Отримати опцію контексту
-   [ZMQContext::getSocket](zmqcontext.getsocket.md) - Створює новий сокет
-   [ZMQContext::isPersistent](zmqcontext.ispersistent.md) — Чи контекст є постійним
-   [ZMQContext::setOpt](zmqcontext.setopt.md) - Встановити опцію сокету
