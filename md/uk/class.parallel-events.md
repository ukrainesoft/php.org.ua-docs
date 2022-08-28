Клас parallelEvents

-   [« parallel\\Channel::close](parallel-channel.close.html)
    
-   [parallel\\Events::setBlocking »](parallel-events.setblocking.html)
    
-   [PHP Manual](index.html)
    
-   [parallel](book.parallel.html)
    
-   Клас parallelEvents
    

# Клас parallelEvents

## Цикл подій

Цикл подій відстежує стан наборів об'єктів Future та/або Channel (цілей) для виконання операцій читання ([parallel\\Future::value()](parallel-future.value.html) [parallel\\Channel::recv()](parallel-channel.recv.html)) та записи ([parallel\\Channel::send()](parallel-channel.send.html)) у міру того, як цілі стають доступними та операції можуть виконуватися без блокування циклу подій.

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

-   [parallel\\Events::setBlocking](parallel-events.setblocking.html) - Поведінка
-   [parallel\\Events::setTimeout](parallel-events.settimeout.html) - Поведінка
-   [parallel\\Events::setInput](parallel-events.setinput.html) - Вхід
-   [parallel\\Events::addChannel](parallel-events.addchannel.html) - Цілі
-   [parallel\\Events::addFuture](parallel-events.addfuture.html) - Цілі
-   [parallel\\Events::remove](parallel-events.remove.html) - Цілі
-   [parallel\\Events::poll](parallel-events.poll.html) - Опитування