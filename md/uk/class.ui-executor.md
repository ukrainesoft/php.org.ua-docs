Планувальник виконання

-   [« UIArea::setSize](ui-area.setsize.html)
    
-   [ОЙExecutor::construct »](ui-executor.construct.html)
    
-   [PHP Manual](index.html)
    
-   [ОЙ](book.ui.html)
    
-   Планувальник виконання
    

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

-   [ОЙExecutor::construct](ui-executor.construct.html) — Створити новий об'єкт Executor
-   [ОЙExecutor::kill](ui-executor.kill.html) - Зупинити виконавець
-   [ОЙExecutor::onExecute](ui-executor.onexecute.html) - Callback-функція виконання
-   [ОЙExecutor::setInterval](ui-executor.setinterval.html) - Управління інтервалом