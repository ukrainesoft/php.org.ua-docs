Клас Threaded

-   [« Предопределённые константы](pthreads.constants.html)
    
-   [Threaded::chunk »](threaded.chunk.html)
    
-   [PHP Manual](index.html)
    
-   [pthreads](book.pthreads.html)
    
-   Клас Threaded
    

# Клас Threaded

(PECL pthreads >= 2.0.0)

## Вступ

Об'єкти Threaded формують базис здатності pthreads запускати код користувача в нових потоках. Клас містить методи синхронізації та різні корисні інтерфейси.

Найважливіше, що Threaded об'єкти забезпечують безпеку для розробника. Усі операції у контексті об'єкта – безпечні.

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

-   [Threaded::chunk](threaded.chunk.html) - Обробка
-   [Threaded::count](threaded.count.html) - Обробка
-   [Threaded::extend](threaded.extend.html) - Обробка під час виконання
-   [Threaded::isRunning](thread.isrunning.html) — Визначення стану
-   [Threaded::isTerminated](threaded.isterminated.html) — Визначення стану
-   [Threaded::merge](threaded.merge.html) - Обробка
-   [Threaded::notify](threaded.notify.html) - Синхронізація
-   [Threaded::notifyOne](threaded.notifyone.html) - Синхронізація
-   [Threaded::pop](threaded.pop.html) - Обробка
-   [Threaded::run](threaded.run.html) - Виконання
-   [Threaded::shift](threaded.shift.html) - Обробка
-   [Threaded::synchronized](threaded.synchronized.html) - Синхронізація
-   [Threaded::wait](threaded.wait.html) - Синхронізація