---
navigation:
  - arrayobject.unserialize.md: '« ArrayObject::unserialize'
  - splobserver.update.md: 'SplObserver::update »'
  - index.md: PHP Manual
  - spl.misc.md: Різні класи та інтерфейси
title: Інтерфейс SplObserver
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс SplObserver

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

## Вступ

Інтерфейс **SplObserver** використовується спільно з [SplSubject](class.splsubject.md)для реализации шаблона проектирования Наблюдатель (Observer).

## Огляд інтерфейсів

```classsynopsis

    
     interface SplObserver {

    /* Методы */
    
   public update(SplSubject $subject): void

   }
```

## Зміст

-   [SplObserver::update](splobserver.update.md) \- Отримати оновлення від суб'єкта
