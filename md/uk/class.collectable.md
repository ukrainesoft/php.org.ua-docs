---
navigation:
  - worker.unstack.md: '« Worker::unstack'
  - collectable.isgarbage.md: 'Collectable::isGarbage »'
  - index.md: PHP Manual
  - book.pthreads.md: pthreads
title: Інтерфейс Collectable
---
# Інтерфейс Collectable

(PECL pthreads >= 2.0.8)

## Вступ

Є об'єкт, який можна зібрати збирачем сміття.

## Огляд інтерфейсів

```classsynopsis


    
    
     
      interface Collectable {
    

    /* Методы */
    
   public isGarbage(): bool


   }
```

## Зміст

-   [Collectable::isGarbage](collectable.isgarbage.md) — Визначає, чи позначений об'єкт як сміття
