Клас Worker

-   [« Thread::start](thread.start.html)
    
-   [Worker::collect »](worker.collect.html)
    
-   [PHP Manual](index.html)
    
-   [pthreads](book.pthreads.html)
    
-   Клас Worker
    

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

-   [Worker::collect](worker.collect.html) — Зібрати посилання на завершені завдання
-   [Worker::getStacked](worker.getstacked.html) — Повертає поточний розмір стека
-   [Worker::isShutdown](worker.isshutdown.html) — Визначення стану
-   [Worker::shutdown](worker.shutdown.html) - Зупинити Worker
-   [Worker::stack](worker.stack.html) - Покласти завдання на стек
-   [Worker::unstack](worker.unstack.html) — Забрати завдання зі стека