---
navigation:
  - swoole-client.wakeup.md: '« SwooleClient::wakeup'
  - swoole-connection-iterator.count.md: 'SwooleConnectionIterator::count »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас SwooleConnectionIterator
---
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

-   [SwooleConnectionIterator::count](swoole-connection-iterator.count.md) - Вважає з'єднання
-   [SwooleConnectionIterator::current](swoole-connection-iterator.current.md) — Повертає поточний запис з'єднання
-   [SwooleConnectionIterator::key](swoole-connection-iterator.key.md) — Повертає ключ поточного з'єднання
-   [SwooleConnectionIterator::next](swoole-connection-iterator.next.md) — Переходить до наступного з'єднання
-   [SwooleConnectionIterator::offsetExists](swoole-connection-iterator.offsetexists.md) — Перевіряє, чи є зміщення
-   [SwooleConnectionIterator::offsetGet](swoole-connection-iterator.offsetget.md) - Зміщення для вилучення
-   [SwooleConnectionIterator::offsetSet](swoole-connection-iterator.offsetset.md) — Призначає з'єднання для зазначеного усунення
-   [SwooleConnectionIterator::offsetUnset](swoole-connection-iterator.offsetunset.md) — скидає зміщення
-   [SwooleConnectionIterator::rewind](swoole-connection-iterator.rewind.md) - Перемотує ітератор
-   [SwooleConnectionIterator::valid](swoole-connection-iterator.valid.md) - Перевіряє правильність поточної позиції
