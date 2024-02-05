---
navigation:
  - class.parallel-events-event.md: « parallel\\Events\\Event
  - class.parallel-sync.md: parallel\\Sync »
  - index.md: PHP Manual
  - book.parallel.md: parallel
title: Клас parallel\\Events\\Event\\Type
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас parallel\\Events\\Event\\Type

(0.9.0)

## Огляд класів

```classsynopsis



    
     
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
