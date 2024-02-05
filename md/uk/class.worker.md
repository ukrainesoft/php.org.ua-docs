---
navigation:
  - thread.start.md: '« Thread::start'
  - worker.collect.md: 'Worker::collect »'
  - index.md: PHP Manual
  - book.pthreads.md: pthreads
title: Клас Worker
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Worker

(PECL pthreads >= 2.0.0)

## Вступ

Робочі потоки мають постійний контекст, тому в більшості випадків їх слід використовувати поверх потоків.

Коли Worker запущено, буде виконано метод run, але Thread не завершиться, доки не буде виконано одну з наступних умов:

-   Worker зникне з області видимості (не залишиться жодного посилання на нього)
    
-   програміст викличе функцію зупинки
    
-   скрипт завершить роботу
    

Це означає, що програміст може перевикористовувати контекст під час виконання. Розміщення об'єкта на стек об'єкта Worker призведе до запуску методу run цього об'єкта.

## Огляд класів

```classsynopsis


    
    
     
      class Worker
     

     
      extends
       Thread
     

     implements 
       Traversable,  Countable,  ArrayAccess {
    

    /* Методы */
    
   public collect(Callable $collector = ?): int
public getStacked(): int
public isShutdown(): bool
public shutdown(): bool
public stack(Threaded &$work): int
public unstack(): int


    /* Наследуемые методы */
    public Thread::getCreatorId(): int
public static Thread::getCurrentThread(): Thread
public static Thread::getCurrentThreadId(): int
public Thread::getThreadId(): int
public Thread::isJoined(): bool
public Thread::isStarted(): bool
public Thread::join(): bool
public Thread::start(int $options = ?): bool


   }
```

## Зміст

-   [Worker::collect](worker.collect.md)— Зібрати посилання на завершені завдання
-   [Worker::getStacked](worker.getstacked.md)— Повертає поточний розмір стека
-   [Worker::isShutdown](worker.isshutdown.md)— Визначення стану
-   [Worker::shutdown](worker.shutdown.md) \- Зупинити Worker
-   [Worker::stack](worker.stack.md) \- Покласти завдання на стек
-   [Worker::unstack](worker.unstack.md)— Забрати завдання зі стека
