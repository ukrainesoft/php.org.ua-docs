---
navigation:
  - fiber.getcurrent.md: '« Fiber::getCurrent'
  - weakreference.construct.md: 'WeakReference::\_\_construct »'
  - index.md: PHP Manual
  - reserved.interfaces.md: Вбудовані інтерфейси та класи
title: Клас WeakReference
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас WeakReference

(PHP 7 >= 7.4.0, PHP 8)

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
$obj = new stdClass;
$weakref = WeakReference::create($obj);
var_dump($weakref->get());
unset($obj);
var_dump($weakref->get());
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(stdClass)#1 (0) {
}
NULL
```

## Зміст

-   [WeakReference::\_\_construct](weakreference.construct.md) \- Конструктор, який забороняє реалізацію
-   [WeakReference::create](weakreference.create.md)— Створює нове слабке посилання
-   [WeakReference::get](weakreference.get.md)— Отримує об'єкт із слабким посиланням
