---
navigation:
  - worker.unstack.md: '« Worker::unstack'
  - collectable.isgarbage.md: 'Collectable::isGarbage »'
  - index.md: PHP Manual
  - book.pthreads.md: pthreads
title: Інтерфейс Collectable
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс Collectable

(PECL pthreads >= 2.0.8)

## Вступ

Представляє об'єкт, який можна зібрати збирачем сміття.

## Огляд інтерфейсів

```classsynopsis


    
    
     
      interface Collectable {
    

    /* Методы */
    
   public isGarbage(): true


   }
```

## Зміст

-   [Collectable::isGarbage](collectable.isgarbage.md)— Визначає, чи позначений об'єкт як сміття
