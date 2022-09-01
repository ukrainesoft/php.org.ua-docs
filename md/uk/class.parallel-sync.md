---
navigation:
  - class.parallel-events-event-type.html: « parallelEventsEventType
  - parallel-sync.construct.html: 'parallelSync::construct »'
  - index.md: PHP Manual
  - book.parallel.md: parallel
title: Клас parallelSync
---
# Клас parallelSync

## Синхронізація низького рівня

Клас **parallelSync** забезпечує доступ до низькорівневих примітивів синхронізації, м'ютексу, умовних змінних і дозволяє реалізувати семафори.

Синхронізація для більшості додатків набагато краще реалізується з використанням каналів, проте в деяких випадках автори коду низькорівневого можуть вважати корисним мати доступ до цих механізмів нижчого рівня.

## Огляд класів

```classsynopsis



    
     
      final
      class parallel\Sync
     
     {


    /* Конструктор */
    
   public __construct()
public __construct(scalar $value)


    /* Доступ */
    public get(): scalar
public set(scalar $value)


    /* Синхронизация */
    public wait()
public notify(bool $all = ?)
public __invoke(callable $critical)


   }
```

## Зміст

-   [parallelSync::construct](parallel-sync.construct.md) - Конструктор класу
-   [parallelSync::get](parallel-sync.get.md) - Доступ
-   [parallelSync::set](parallel-sync.set.md) - Доступ
-   [parallelSync::wait](parallel-sync.wait.md) - Синхронізація
-   [parallelSync::notify](parallel-sync.notify.md) - Синхронізація
-   [parallelSync::invoke](parallel-sync.invoke.md) - Синхронізація
