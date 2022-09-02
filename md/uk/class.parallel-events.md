---
navigation:
  - parallel-channel.close.md: '« parallelChannel::close'
  - parallel-events.setblocking.md: 'parallelEvents::setBlocking »'
  - index.md: PHP Manual
  - book.parallel.md: parallel
title: Клас parallelEvents
---
# Клас parallelEvents

## Цикл подій

Цикл подій відстежує стан наборів об'єктів Future та/або Channel (цілей) для виконання операцій читання ([parallelFuture::value()](parallel-future.value.md) [parallelChannel::recv()](parallel-channel.recv.md)) та записи ([parallelChannel::send()](parallel-channel.send.md)) у міру того, як цілі стають доступними та операції можуть виконуватися без блокування циклу подій.

## Огляд класів

```classsynopsis



    
     
      final
      class parallel\Events
     
     implements 
       Countable,  Traversable {


    /* Входные данные */
    
   public setInput(Input $input): void


    /* Цели */
    public addChannel(parallel\Channel $channel): void
public addFuture(string $name, parallel\Future $future): void
public remove(string $target): void


    /* Поведение */
    public setBlocking(bool $blocking): void
public setTimeout(int $timeout): void


    /* Опрос */
    public poll(): ?parallel\Events\Event

   }
```

## Зміст

-   [parallelEvents::setBlocking](parallel-events.setblocking.md) - Поведінка
-   [parallelEvents::setTimeout](parallel-events.settimeout.md) - Поведінка
-   [parallelEvents::setInput](parallel-events.setinput.md) - Вхід
-   [parallelEvents::addChannel](parallel-events.addchannel.md) - Цілі
-   [parallelEvents::addFuture](parallel-events.addfuture.md) - Цілі
-   [parallelEvents::remove](parallel-events.remove.md) - Цілі
-   [parallelEvents::poll](parallel-events.poll.md) - Опитування
