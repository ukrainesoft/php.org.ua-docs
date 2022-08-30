Клас EventConfig

-   [« О callback-функциях событийного буфера](eventbufferevent.about.callbacks.html)
    
-   [EventConfig::avoidMethod »](eventconfig.avoidmethod.html)
    
-   [PHP Manual](index.html)
    
-   [Event](book.event.html)
    
-   Клас EventConfig
    

# Клас EventConfig

(PECL event >= 1.2.6-beta)

## Вступ

Представляє структуру, яку можна використовувати під час створення [EventBase](class.eventbase.html)

## Огляд класів

```classsynopsis

     
    
    
    
     
      final
      class EventConfig
     
     {
    
    /* Константы */
    
     const
     int
      FEATURE_ET = 1;

    const
     int
      FEATURE_O1 = 2;

    const
     int
      FEATURE_FDS = 4;

    /* Методы */
    
   public
   avoidMethod(
    string
     $method
   ): bool
public
   __construct()
public
   requireFeatures(
    int
     $feature
   ): bool
public
   setFlags(
    int
     $flags
   ): bool
public
   setMaxDispatchInterval(
    int
     $max_interval
   , 
    int
     $max_callbacks
   , 
    int
     $min_priority
   ): void

   }
```

## Обумовлені константи

**`EventConfig::FEATURE_ET`**

Потрібний метод бекенда, що підтримує одноразове спрацювання при тривалій події (edge-triggered I/O).

**`EventConfig::FEATURE_O1`**

Потрібний метод бекенда, для якого видалення, додавання або перемикання події в активний статус має складність O(1).

**`EventConfig::FEATURE_FDS`**

Потрібний метод бекенда, що підтримує звичайні файлові дескриптори, а не тільки сокети.

## Зміст

-   [EventConfig::avoidMethod](eventconfig.avoidmethod.html) — Попросити libevent не використати певний метод події
-   [EventConfig::construct](eventconfig.construct.html) — Створити об'єкт EventConfig
-   [EventConfig::requireFeatures](eventconfig.requirefeatures.html) — Ввести необхідні додатки властивості методу події
-   [EventConfig::setFlags](eventconfig.setflags.html) — Встановлює один або кілька прапорів для налаштування можливої ​​ініціалізації EventBase
-   [EventConfig::setMaxDispatchInterval](eventconfig.setmaxdispatchinterval.html) — Запобігти інверсії пріоритетів