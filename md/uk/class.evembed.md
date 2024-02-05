---
navigation:
  - evchild.set.md: '« EvChild::set'
  - evembed.construct.md: 'EvEmbed::\_\_construct »'
  - index.md: PHP Manual
  - book.ev.md: Ev
title: Клас EvEmbed
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас EvEmbed

(PECL ev >= 0.2.0)

## Вступ

Використовується для вставлення одного циклу подій в інший.

## Огляд класів

```classsynopsis

     
    
    
    
     
      class EvEmbed
     
     
      extends
       EvWatcher
     
     {
    
    /* Свойства */
    
     public
      $embed;

    /* Методы */
    
   public
   __construct(    
    object
     $other
   ,    
    callable
     $callback
    = ?,    
    mixed
     $data
    = ?,    
    int
     $priority
    = ?)

    final
   public
   static
   createStopped(    
    object
     $other
   ,    
    callable
     $callback
    = ?,    
    mixed
     $data
    = ?,    
    int
     $priority
    = ?): void
public
   set(
    object
     $other
   ): void
public
   sweep(): void

    /* Наследуемые методы */
    public
   EvWatcher::clear(): int
public
   EvWatcher::feed(
    int
     $revents
   ): void
public
   EvWatcher::getLoop(): EvLoop
public
   EvWatcher::invoke(
    int
     $revents
   ): void
public
   EvWatcher::keepalive(
    bool
     $value
    = ?): bool
public
   EvWatcher::setCallback(
    callable
     $callback
   ): void
public
   EvWatcher::start(): void
public
   EvWatcher::stop(): void

   }
```

## Властивості

is\_active

data

is\_pending

priority

embed

## Зміст

-   [EvEmbed::\_\_construct](evembed.construct.md) \- Конструктор об'єкта EvEmbed
-   [EvEmbed::createStopped](evembed.createstopped.md)— Створює зупинений об'єкт спостерігач EvEmbed
-   [EvEmbed::set](evembed.set.md)— Налаштування спостерігача
-   [EvEmbed::sweep](evembed.sweep.md)— Робить одиночну, неблокуючу розгортку за вбудованим циклом
