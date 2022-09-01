---
navigation:
  - ui-area.setsize.html: '« UIArea::setSize'
  - ui-executor.construct.html: 'ОЙExecutor::construct »'
  - index.md: PHP Manual
  - book.ui.md: ОЙ
title: Планувальник виконання
---
# Планувальник виконання

(UI 2.0.0)

## Вступ

Ця можливість планує повторне виконання callback-функції, корисне для анімації та інших подібних дій.

## Огляд класів

```classsynopsis



    
     
      abstract
      class UI\Executor
     
     {


    /* Конструктор */
    
   public __construct()
public __construct(int $microseconds)
public __construct(int $seconds, int $microseconds)


    /* Методы */
    public kill(): void
abstract protected onExecute(): void
public setInterval(int $microseconds): bool
public setInterval(int $seconds, int $microseconds): bool

   }
```

## Зміст

-   [ОЙExecutor::construct](ui-executor.construct.md) — Створити новий об'єкт Executor
-   [ОЙExecutor::kill](ui-executor.kill.md) - Зупинити виконавець
-   [ОЙExecutor::onExecute](ui-executor.onexecute.md) - Callback-функція виконання
-   [ОЙExecutor::setInterval](ui-executor.setinterval.md) - Управління інтервалом
