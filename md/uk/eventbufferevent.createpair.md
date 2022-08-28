Створює дві буферні події, пов'язані один з одним

-   [« EventBufferEvent::\_\_construct](eventbufferevent.construct.html)
    
-   [EventBufferEvent::disable »](eventbufferevent.disable.html)
    
-   [PHP Manual](index.html)
    
-   [EventBufferEvent](class.eventbufferevent.html)
    
-   Створює дві буферні події, пов'язані один з одним
    

# EventBufferEvent::createPair

(PECL event >= 1.2.6-beta)

EventBufferEvent::createPair — Створює дві буферні події, пов'язані один з одним

### Опис

```methodsynopsis
public
   static
   EventBufferEvent::createPair(
    EventBase
     $base
   , 
    int
     $options
     = 0
   ): array
```

Повертає масив із двох об'єктів [EventBufferEvent](class.eventbufferevent.html), пов'язані один з одним. Підтримуються всі звичайні параметри, крім **`EventBufferEvent::OPT_CLOSE_ON_FREE`**, який не діє, та **`EventBufferEvent::OPT_DEFER_CALLBACKS`**, який завжди включено.

### Список параметрів

`base`

Пов'язана основа подій.

`options`

Константи EventBufferEvent::OPT у поєднанні з побітовим АБО (`OR`

### Значення, що повертаються

Повертає масив із двох об'єктів [EventBufferEvent](class.eventbufferevent.html), пов'язані один з одним.

### список змін

| Версия           | Описание              |
|------------------|-----------------------|
| PECL event 1.9.0 | Метод став статичним. |