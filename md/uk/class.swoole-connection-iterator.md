Клас SwooleConnectionIterator

-   [« Swoole\\Client::wakeup](swoole-client.wakeup.html)
    
-   [Swoole\\Connection\\Iterator::count »](swoole-connection-iterator.count.html)
    
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

-   [Swoole\\Connection\\Iterator::count](swoole-connection-iterator.count.html) - Вважає з'єднання
-   [Swoole\\Connection\\Iterator::current](swoole-connection-iterator.current.html) — Повертає поточний запис з'єднання
-   [Swoole\\Connection\\Iterator::key](swoole-connection-iterator.key.html) — Повертає ключ поточного з'єднання
-   [Swoole\\Connection\\Iterator::next](swoole-connection-iterator.next.html) — Переходить до наступного з'єднання
-   [Swoole\\Connection\\Iterator::offsetExists](swoole-connection-iterator.offsetexists.html) — Перевіряє, чи є зміщення
-   [Swoole\\Connection\\Iterator::offsetGet](swoole-connection-iterator.offsetget.html) - Зміщення для вилучення
-   [Swoole\\Connection\\Iterator::offsetSet](swoole-connection-iterator.offsetset.html) — Призначає з'єднання для зазначеного усунення
-   [Swoole\\Connection\\Iterator::offsetUnset](swoole-connection-iterator.offsetunset.html) — скидає зміщення
-   [Swoole\\Connection\\Iterator::rewind](swoole-connection-iterator.rewind.html) - Перемотує ітератор
-   [Swoole\\Connection\\Iterator::valid](swoole-connection-iterator.valid.html) - Перевіряє правильність поточної позиції