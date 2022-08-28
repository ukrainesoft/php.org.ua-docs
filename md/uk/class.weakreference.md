Клас WeakReference

-   [« Fiber::getCurrent](fiber.getcurrent.html)
    
-   [WeakReference::\_\_construct »](weakreference.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Встроенные интерфейсы и классы](reserved.interfaces.html)
    
-   Клас WeakReference
    

# Клас WeakReference

(PHP 7> = 7.4.0, PHP 8)

## Вступ

Клас WeakReference надає спосіб доступу до об'єкта, не впливаючи на кількість посилань на нього, таким чином збирач сміття зможе звільнити цей об'єкт.

Об'єкт класу **WeakReference** не може бути серіалізованим.

## Огляд класів

```classsynopsis

     
    

    
     
      final
      class WeakReference
     
     {

    /* Методы */
    
   public __construct()

    public static create(object $object): WeakReference
public get(): ?object

   }
```

## Приклади використання WeakReference

**приклад #1 приклад #1. Просте використання WeakReference**

```php
<?php
$obj = new stdClass;
$weakref = WeakReference::create($obj);
var_dump($weakref->get());
unset($obj);
var_dump($weakref->get());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(stdClass)#1 (0) {
}
NULL
```

## Зміст

-   [WeakReference::\_\_construct](weakreference.construct.html) - Конструктор, який забороняє реалізацію
-   [WeakReference::create](weakreference.create.html) — Створює нове слабке посилання
-   [WeakReference::get](weakreference.get.html) — Отримує об'єкт із слабким посиланням