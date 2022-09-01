---
navigation:
  - zmqsocket.unbind.md: '« ZMQSocket::unbind'
  - zmqpoll.add.md: 'ZMQPoll::add »'
  - index.md: PHP Manual
  - book.zmq.md: Обмін повідомленнями 0MQ
title: Клас ZMQPoll
---
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

-   [ZMQPoll::add](zmqpoll.add.md) — Додати елемент у пул опитування
-   [ZMQPoll::clear](zmqpoll.clear.md) - Очистити пул опитування
-   [ZMQPoll::count](zmqpoll.count.md) — Кількість елементів у пулі опитування
-   [ZMQPoll::getLastErrors](zmqpoll.getlasterrors.md) — Повертає помилки останнього опитування
-   [ZMQPoll::poll](zmqpoll.poll.md) — Опитати всі елементи пулу
-   [ZMQPoll::remove](zmqpoll.remove.md) — Видалити елемент із пулу опитування
