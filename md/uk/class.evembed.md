---
navigation:
  - evchild.set.html: '« EvChild::set'
  - evembed.construct.html: 'EvEmbed::construct »'
  - index.html: PHP Manual
  - book.ev.html: Єв
title: Клас EvEmbed
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

ісactive

data

ісpending

priority

embed

## Зміст

-   [EvEmbed::construct](evembed.construct.html) - Конструктор об'єкта EvEmbed
-   [EvEmbed::createStopped](evembed.createstopped.html) — Створює зупинений об'єкт спостерігач EvEmbed
-   [EvEmbed::set](evembed.set.html) — Налаштування спостерігача
-   [EvEmbed::sweep](evembed.sweep.html) — Робить одиночну, неблокуючу розгортку за вбудованим циклом
