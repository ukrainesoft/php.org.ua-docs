---
navigation:
  - splobserver.update.md: '« SplObserver::update'
  - splsubject.attach.md: 'SplSubject::attach »'
  - index.md: PHP Manual
  - spl.misc.md: Різні класи та інтерфейси
title: Інтерфейс SplSubject
---
# Інтерфейс SplSubject

(PHP 5> = 5.1.0, PHP 7, PHP 8)

## Вступ

Інтерфейс **SplSubject** використовується спільно з [SplObserver](class.splobserver.md) для реалізації шаблону проектування Спостерігач (Observer).

## Огляд інтерфейсів

```classsynopsis

     
    

    
     
      interface SplSubject {

    /* Методы */
    
   public attach(SplObserver $observer): void
public detach(SplObserver $observer): void
public notify(): void

   }
```

## Зміст

-   [SplSubject::attach](splsubject.attach.md) — Приєднати спостерігача (об'єкт класу SplObserver)
-   [SplSubject::detach](splsubject.detach.md) — Від'єднати спостерігача
-   [SplSubject::notify](splsubject.notify.md) — повідомити спостерігача
