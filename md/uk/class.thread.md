---
navigation:
  - threaded.wait.md: '« Threaded::wait'
  - thread.getcreatorid.md: 'Thread::getCreatorId »'
  - index.md: PHP Manual
  - book.pthreads.md: pthreads
title: Клас Thread
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Thread

(PECL pthreads >= 2.0.0)

## Вступ

Коли викликаний стартовий метод Thread, код методу run буде запущений окремому потоці, паралельно.

Після відпрацювання методу run, Thread відразу завершить роботу. Він буде приєднаний шляхом створення Thread у потрібний час.

**Увага**

Якщо покладатися на двигун визначення, коли Thread буде приєднаний, можна зіткнутися з несподіваним поведінкою. Тому необхідно, по можливості, керувати приєднанням у явному вигляді.

## Огляд класів

```classsynopsis


    
    
     
      class Thread
     

     
      extends
       Threaded
     

     implements 
       Countable,  Traversable,  ArrayAccess {
    

    /* Методы */
    
   public getCreatorId(): int
public static getCurrentThread(): Thread
public static getCurrentThreadId(): int
public getThreadId(): int
public isJoined(): bool
public isStarted(): bool
public join(): bool
public start(int $options = ?): bool


    /* Наследуемые методы */
    public Threaded::chunk(int $size, bool $preserve): array
public Threaded::count(): int
public Threaded::extend(string $class): bool
public Threaded::isRunning(): bool
public Threaded::isTerminated(): bool
public Threaded::merge(mixed $from, bool $overwrite = ?): bool
public Threaded::notify(): bool
public Threaded::notifyOne(): bool
public Threaded::pop(): bool
public Threaded::run(): void
public Threaded::shift(): mixed
public Threaded::synchronized(Closure $block, mixed ...$args): mixed
public Threaded::wait(int $timeout = ?): bool


   }
```

## Зміст

-   [Thread::getCreatorId](thread.getcreatorid.md) \- Ідентифікація
-   [Thread::getCurrentThread](thread.getcurrentthread.md) \- Ідентифікація
-   [Thread::getCurrentThreadId](thread.getcurrentthreadid.md) \- Ідентифікація
-   [Thread::getThreadId](thread.getthreadid.md) \- Ідентифікація
-   [Thread::isJoined](thread.isjoined.md)— Визначення стану
-   [Thread::isStarted](thread.isstarted.md)— Визначення стану
-   [Thread::join](thread.join.md) \- Синхронізація
-   [Thread::start](thread.start.md) \- Виконання
