---
navigation:
  - parallel-events-input.remove.md: '« parallel\\Events\\Input::remove'
  - class.parallel-events-event-type.md: parallel\\Events\\Event\\Type »
  - index.md: PHP Manual
  - book.parallel.md: parallel
title: Клас parallel\\Events\\Event
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас parallel\\Events\\Event

(0.9.0)

## Об'єкти подій

Коли повертається об'єкт Event, Event::$object має бути видалено з циклу, який його повернув, якщо подія є подією запису, клас **Input** екземпляра Event::$source також слід видалити.

## Огляд класів

```classsynopsis



    
     
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
