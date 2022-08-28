Інтерфейс SplObserver

-   [« ArrayObject::unserialize](arrayobject.unserialize.html)
    
-   [SplObserver::update »](splobserver.update.html)
    
-   [PHP Manual](index.html)
    
-   [Различные классы и интерфейсы](spl.misc.html)
    
-   Інтерфейс SplObserver
    

# Інтерфейс SplObserver

(PHP 5> = 5.1.0, PHP 7, PHP 8)

## Вступ

Інтерфейс **SplObserver** використовується спільно з [SplSubject](class.splsubject.html) для реалізації шаблону проектування Спостерігач (Observer).

## Огляд інтерфейсів

```classsynopsis

     
    

    
     
      interface SplObserver {

    /* Методы */
    
   public update(SplSubject $subject): void

   }
```

## Зміст

-   [SplObserver::update](splobserver.update.html) - Отримати оновлення від суб'єкта