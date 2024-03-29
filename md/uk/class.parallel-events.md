---
navigation:
  - parallel-channel.close.md: '« parallel\\Channel::close'
  - parallel-events.setblocking.md: 'parallel\\Events::setBlocking »'
  - index.md: PHP Manual
  - book.parallel.md: parallel
title: Клас parallel\\Events
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас parallel\\Events

(0.9.0)

## Цикл подій

Цикл подій відстежує стан наборів об'єктів Future та/або Channel (цілей) для виконання операцій читання ([parallel\\Future::value()](parallel-future.value.md) [parallel\\Channel::recv()](parallel-channel.recv.md)) та записи ([parallel\\Channel::send()](parallel-channel.send.md)) у міру того, як цілі стають доступними та операції можуть виконуватися без блокування циклу подій.

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

-   [parallel\\Events::setBlocking](parallel-events.setblocking.md) \- Поведінка
-   [parallel\\Events::setTimeout](parallel-events.settimeout.md) \- Поведінка
-   [parallel\\Events::setInput](parallel-events.setinput.md) \- Вхід
-   [parallel\\Events::addChannel](parallel-events.addchannel.md) \- Цілі
-   [parallel\\Events::addFuture](parallel-events.addfuture.md) \- Цілі
-   [parallel\\Events::remove](parallel-events.remove.md) \- Цілі
-   [parallel\\Events::poll](parallel-events.poll.md) \- Опитування
