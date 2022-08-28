Інтерфейс SplSubject

-   [« SplObserver::update](splobserver.update.html)
    
-   [SplSubject::attach »](splsubject.attach.html)
    
-   [PHP Manual](index.html)
    
-   [Различные классы и интерфейсы](spl.misc.html)
    
-   Інтерфейс SplSubject
    

# Інтерфейс SplSubject

(PHP 5> = 5.1.0, PHP 7, PHP 8)

## Вступ

Інтерфейс **SplSubject** використовується спільно з [SplObserver](class.splobserver.html) для реалізації шаблону проектування Спостерігач (Observer).

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

-   [SplSubject::attach](splsubject.attach.html) — Приєднати спостерігача (об'єкт класу SplObserver)
-   [SplSubject::detach](splsubject.detach.html) — Від'єднати спостерігача
-   [SplSubject::notify](splsubject.notify.html) — повідомити спостерігача