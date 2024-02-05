---
navigation:
  - ui-area.setsize.md: '« UI\\Area::setSize'
  - ui-executor.construct.md: 'UI\\Executor::\_\_construct »'
  - index.md: PHP Manual
  - book.ui.md: UI
title: Планувальник виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

-   [UI\\Executor::\_\_construct](ui-executor.construct.md)— Створити новий об'єкт Executor
-   [UI\\Executor::kill](ui-executor.kill.md) \- Зупинити виконавець
-   [UI\\Executor::onExecute](ui-executor.onexecute.md) \- Callback-функція виконання
-   [UI\\Executor::setInterval](ui-executor.setinterval.md) \- Управління інтервалом
