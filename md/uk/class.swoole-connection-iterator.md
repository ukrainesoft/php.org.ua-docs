Клас SwooleConnectionIterator

-   [« SwooleClient::wakeup](swoole-client.wakeup.html)
    
-   [SwooleConnectionIterator::count »](swoole-connection-iterator.count.html)
    
-   [PHP Manual](index.html)
    
-   [Swoole](book.swoole.html)
    
-   Клас SwooleConnectionIterator
    

# Клас SwooleConnectionIterator

(PECL swoole >= 1.9.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class Swoole\Connection\Iterator
     

     implements 
       Iterator,  Countable,  ArrayAccess {


    /* Методы */
    
   public count(): int
public current(): Connection
public key(): int
public next(): Connection
public offsetExists(int $index): bool
public offsetGet(string $index): Connection
public offsetSet(int $offset, mixed $connection): void
public offsetUnset(int $offset): void
public rewind(): void
public valid(): bool

   }
```

## Зміст

-   [SwooleConnectionIterator::count](swoole-connection-iterator.count.html) - Вважає з'єднання
-   [SwooleConnectionIterator::current](swoole-connection-iterator.current.html) — Повертає поточний запис з'єднання
-   [SwooleConnectionIterator::key](swoole-connection-iterator.key.html) — Повертає ключ поточного з'єднання
-   [SwooleConnectionIterator::next](swoole-connection-iterator.next.html) — Переходить до наступного з'єднання
-   [SwooleConnectionIterator::offsetExists](swoole-connection-iterator.offsetexists.html) — Перевіряє, чи є зміщення
-   [SwooleConnectionIterator::offsetGet](swoole-connection-iterator.offsetget.html) - Зміщення для вилучення
-   [SwooleConnectionIterator::offsetSet](swoole-connection-iterator.offsetset.html) — Призначає з'єднання для зазначеного усунення
-   [SwooleConnectionIterator::offsetUnset](swoole-connection-iterator.offsetunset.html) — скидає зміщення
-   [SwooleConnectionIterator::rewind](swoole-connection-iterator.rewind.html) - Перемотує ітератор
-   [SwooleConnectionIterator::valid](swoole-connection-iterator.valid.html) - Перевіряє правильність поточної позиції