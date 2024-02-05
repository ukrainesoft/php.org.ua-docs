---
navigation:
  - eventbufferevent.about.callbacks.md: Про callback-функції подієвого буфера
  - eventconfig.avoidmethod.md: 'EventConfig::avoidMethod »'
  - index.md: PHP Manual
  - book.event.md: Event
title: Клас EventConfig
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас EventConfig

(PECL event >= 1.2.6-beta)

## Вступ

Представляє структуру конфігурації, яку передають конструктор класу [EventBase](class.eventbase.md)

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

-   [EventConfig::avoidMethod](eventconfig.avoidmethod.md)— Попросити libevent не використати певний метод події
-   [EventConfig::\_\_construct](eventconfig.construct.md)— Створити об'єкт EventConfig
-   [EventConfig::requireFeatures](eventconfig.requirefeatures.md)— Ввести необхідні додатки властивості методу події
-   [EventConfig::setFlags](eventconfig.setflags.md)— Встановлює один або кілька прапорів для налаштування можливої ​​ініціалізації EventBase
-   [EventConfig::setMaxDispatchInterval](eventconfig.setmaxdispatchinterval.md)— Запобігти інверсії пріоритетів
