---
navigation:
  - pthreads.constants.md: « Зумовлені константи
  - threaded.chunk.md: 'Threaded::chunk »'
  - index.md: PHP Manual
  - book.pthreads.md: pthreads
title: Клас Threaded
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Threaded

(PECL pthreads >= 2.0.0)

## Вступ

Об'єкти Threaded формують базис здатності pthreads запускати код користувача в нових потоках. Клас містить методи синхронізації та різні корисні інтерфейси.

Найважливіше, що об'єкти Threaded забезпечують безпеку для розробника. Усі операції у контексті об'єкта – безпечні.

## Огляд класів

```classsynopsis


    
    
     
      class Threaded
     

     implements 
       Collectable,  Traversable,  Countable,  ArrayAccess {
    

    /* Методы */
    
   public chunk(int $size, bool $preserve): array
public count(): int
public extend(string $class): bool
public isRunning(): bool
public isTerminated(): bool
public merge(mixed $from, bool $overwrite = ?): bool
public notify(): bool
public notifyOne(): bool
public pop(): bool
public run(): void
public shift(): mixed
public synchronized(Closure $block, mixed ...$args): mixed
public wait(int $timeout = ?): bool

   }
```

## Зміст

-   [Threaded::chunk](threaded.chunk.md) \- Обробка
-   [Threaded::count](threaded.count.md) \- Обробка
-   [Threaded::extend](threaded.extend.md) \- Обробка під час виконання
-   [Threaded::isRunning](thread.isrunning.md)— Визначення стану
-   [Threaded::isTerminated](threaded.isterminated.md)— Визначення стану
-   [Threaded::merge](threaded.merge.md) \- Обробка
-   [Threaded::notify](threaded.notify.md) \- Синхронізація
-   [Threaded::notifyOne](threaded.notifyone.md) \- Синхронізація
-   [Threaded::pop](threaded.pop.md) \- Обробка
-   [Threaded::run](threaded.run.md) \- Виконання
-   [Threaded::shift](threaded.shift.md) \- Обробка
-   [Threaded::synchronized](threaded.synchronized.md) \- Синхронізація
-   [Threaded::wait](threaded.wait.md) \- Синхронізація
