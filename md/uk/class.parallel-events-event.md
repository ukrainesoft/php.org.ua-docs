Клас parallelEventsEvent

-   [« parallelEventsInput::remove](parallel-events-input.remove.html)
    
-   [parallelEventsEventType »](class.parallel-events-event-type.html)
    
-   [PHP Manual](index.html)
    
-   [parallel](book.parallel.html)
    
-   Клас parallelEventsEvent
    

# Клас parallelEventsEvent

## Об'єкти подій

Коли повертається об'єкт Event, Event::$object має бути видалено з циклу, який його повернув, якщо подія є подією запису, клас **Input** екземпляра Event::$source також слід видалити.

## Огляд класів

```synopsis



    
     
      final
      class parallel\Events\Event
     
     {


    /* Одна из констант Event\Type. */
    
     public
     int
      $type;


    /* Должен быть источником события (имя цели) */
    public
     string
      $source;


    /* Должно быть либо Future, либо Channel */
    public
     object
      $object;


    /* Должен быть установлен для событий чтения/ошибки */
    public
      $value;


   }
```