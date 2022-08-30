Клас parallelEventsEventType

-   [« parallelEventsEvent](class.parallel-events-event.html)
    
-   [parallelSync »](class.parallel-sync.html)
    
-   [PHP Manual](index.html)
    
-   [parallel](book.parallel.html)
    
-   Клас parallelEventsEventType
    

# Клас parallelEventsEventType

## Огляд класів

```synopsis



    
     
      final
      class parallel\Events\Event\Type
     
     {


    /* Event::$object был прочитан в Event::$value */
    
     const
      Read;


    /* Input for Event::$source записан в Event::$object */
    const
      Write;


    /* Event::$object (Канал) был закрыт */
    const
      Close;


    /* Event::$object (Фьючерс) был прекращён */
    const
      Cancel;


    /* Среда выполнения, выполняющая Event::$object (Фьючерс), была уничтожена */
    const
      Kill;


    /* Event::$object (фьючерс) выдал ошибку */
    const
      Error;


   }
```