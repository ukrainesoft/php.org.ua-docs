Інтерфейс SplObserver

-   [« ArrayObject::unserialize](arrayobject.unserialize.md)
    
-   [SplObserver::update »](splobserver.update.md)
    
-   [PHP Manual](index.md)
    
-   [Різні класи та інтерфейси](spl.misc.md)
    
-   Інтерфейс SplObserver
    

# Інтерфейс SplObserver

(PHP 5> = 5.1.0, PHP 7, PHP 8)

## Вступ

Інтерфейс **SplObserver** використовується спільно з [SplSubject](class.splsubject.md) для реалізації шаблону проектування Спостерігач (Observer).

## Огляд інтерфейсів

```classsynopsis

     
    

    
     
      interface SplObserver {

    /* Методы */
    
   public update(SplSubject $subject): void

   }
```

## Зміст

-   [SplObserver::update](splobserver.update.md) - Отримати оновлення від суб'єкта