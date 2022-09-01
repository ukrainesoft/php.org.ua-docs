---
navigation:
  - collectable.isgarbage.md: '« Collectable::isGarbage'
  - pool.collect.md: 'Pool::collect »'
  - index.md: PHP Manual
  - book.pthreads.md: pthreads
title: Клас Pool
---
# Клас Pool

(PECL pthreads >= 2.0.0)

## Вступ

Об'єкт Pool є контейнером для зберігання об'єктів Worker, управління ними та регулювання їхньої кількості.

Контейнеризація являє собою найвищий рівень абстракції над функціоналом Worker, включаючи управління посиланнями в коректному для pthreads вигляді.

## Огляд класів

```classsynopsis


    
    
     
      class Pool
     
     {
    
    /* Свойства */
    
     protected
      $size;

    protected
      $class;

    protected
      $workers;

    protected
      $ctor;

    protected
      $last;



    /* Методы */
    
   public __construct(int $size, string $class = ?, array $ctor = ?)

    public collect(Callable $collector = ?): int
public resize(int $size): void
public shutdown(): void
public submit(Threaded $task): int
public submitTo(int $worker, Threaded $task): int

   }
```

## Властивості

size

максимальна кількість об'єктів Worker

class

клас Worker

workers

посилання на об'єкти Worker

ctor

аргументи конструктора нових об'єктів Worker

last

зміщення останнього використаного Worker у workers

## Зміст

-   [Pool::collect](pool.collect.md) — Збирає посилання на виконані завдання
-   [Pool::construct](pool.construct.md) - Створює новий пул воркерів
-   [Pool::resize](pool.resize.md) - Змінює розмір пулу
-   [Pool::shutdown](pool.shutdown.md) - Вимикає всі воркери
-   [Pool::submit](pool.submit.md) - Відправляє об'єкт на виконання
-   [Pool::submitTo](pool.submitTo.md) — Надсилає завдання конкретному воркеру для виконання
