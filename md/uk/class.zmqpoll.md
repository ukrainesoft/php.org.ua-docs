Клас ZMQPoll

-   [« ZMQSocket::unbind](zmqsocket.unbind.html)
    
-   [ZMQPoll::add »](zmqpoll.add.html)
    
-   [PHP Manual](index.html)
    
-   [Обмен сообщениями 0MQ](book.zmq.html)
    
-   Клас ZMQPoll
    

# Клас ZMQPoll

(PECL zmq >= 0.5.0)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class ZMQPoll
     
     {
    

    /* Методы */
    
   public add(mixed $entry, int $type): string
public clear(): ZMQPoll
public count(): int
public getLastErrors(): array
public poll(array &$readable, array &$writable, int $timeout = -1): int
public remove(mixed $item): bool

   }
```

## Зміст

-   [ZMQPoll::add](zmqpoll.add.html) — Додати елемент у пул опитування
-   [ZMQPoll::clear](zmqpoll.clear.html) - Очистити пул опитування
-   [ZMQPoll::count](zmqpoll.count.html) — Кількість елементів у пулі опитування
-   [ZMQPoll::getLastErrors](zmqpoll.getlasterrors.html) — Повертає помилки останнього опитування
-   [ZMQPoll::poll](zmqpoll.poll.html) — Опитати всі елементи пулу
-   [ZMQPoll::remove](zmqpoll.remove.html) — Видалити елемент із пулу опитування