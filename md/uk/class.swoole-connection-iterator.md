---
navigation:
  - swoole-client.wakeup.md: '« Swoole\\Client::wakeup'
  - swoole-connection-iterator.count.md: 'Swoole\\Connection\\Iterator::count »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас Swoole\\Connection\\Iterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Swoole\\Connection\\Iterator

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

-   [Swoole\\Connection\\Iterator::count](swoole-connection-iterator.count.md) \- Вважає з'єднання
-   [Swoole\\Connection\\Iterator::current](swoole-connection-iterator.current.md)— Повертає поточний запис з'єднання
-   [Swoole\\Connection\\Iterator::key](swoole-connection-iterator.key.md)— Повертає ключ поточного з'єднання
-   [Swoole\\Connection\\Iterator::next](swoole-connection-iterator.next.md)— Переходить до наступного з'єднання
-   [Swoole\\Connection\\Iterator::offsetExists](swoole-connection-iterator.offsetexists.md)— Перевіряє, чи є зміщення
-   [Swoole\\Connection\\Iterator::offsetGet](swoole-connection-iterator.offsetget.md) \- Зміщення для вилучення
-   [Swoole\\Connection\\Iterator::offsetSet](swoole-connection-iterator.offsetset.md)— Призначає з'єднання для зазначеного усунення
-   [Swoole\\Connection\\Iterator::offsetUnset](swoole-connection-iterator.offsetunset.md)— скидає зміщення
-   [Swoole\\Connection\\Iterator::rewind](swoole-connection-iterator.rewind.md) \- Перемотує ітератор
-   [Swoole\\Connection\\Iterator::valid](swoole-connection-iterator.valid.md) \- Перевіряє правильність поточної позиції
