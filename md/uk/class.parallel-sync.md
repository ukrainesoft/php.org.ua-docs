Клас parallelSync

-   [« parallel\\Events\\Event\\Type](class.parallel-events-event-type.html)
    
-   [parallel\\Sync::\_\_construct »](parallel-sync.construct.html)
    
-   [PHP Manual](index.html)
    
-   [parallel](book.parallel.html)
    
-   Клас parallelSync
    

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

-   [parallel\\Sync::\_\_construct](parallel-sync.construct.html) - Конструктор класу
-   [parallel\\Sync::get](parallel-sync.get.html) - Доступ
-   [parallel\\Sync::set](parallel-sync.set.html) - Доступ
-   [parallel\\Sync::wait](parallel-sync.wait.html) - Синхронізація
-   [parallel\\Sync::notify](parallel-sync.notify.html) - Синхронізація
-   [parallel\\Sync::\_\_invoke](parallel-sync.invoke.html) - Синхронізація