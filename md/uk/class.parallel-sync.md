---
navigation:
  - class.parallel-events-event-type.md: « parallel\\Events\\Event\\Type
  - parallel-sync.construct.md: 'parallel\\Sync::\_\_construct »'
  - index.md: PHP Manual
  - book.parallel.md: parallel
title: Клас parallel\\Sync
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас parallel\\Sync

(1.1.0)

## Синхронізація низького рівня

Класс**parallel\\Sync** забезпечує доступ до низькорівневих примітивів синхронізації, м'ютексу, умовних змінних і дозволяє реалізувати семафори.

Синхронізація для більшості додатків набагато краще реалізується з використанням каналів, проте в деяких випадках автори кодів низького рівня можуть вважати корисним мати доступ до цих механізмів нижчого рівня.

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

-   [parallel\\Sync::\_\_construct](parallel-sync.construct.md) \- Конструктор класу
-   [parallel\\Sync::get](parallel-sync.get.md) \- Доступ
-   [parallel\\Sync::set](parallel-sync.set.md) \- Доступ
-   [parallel\\Sync::wait](parallel-sync.wait.md) \- Синхронізація
-   [parallel\\Sync::notify](parallel-sync.notify.md) \- Синхронізація
-   [parallel\\Sync::\_\_invoke](parallel-sync.invoke.md) \- Синхронізація
