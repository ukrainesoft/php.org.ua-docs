---
navigation:
  - serializable.unserialize.md: '« Serializable::unserialize'
  - closure.construct.md: 'Closure::\_\_construct »'
  - index.md: PHP Manual
  - reserved.interfaces.md: Вбудовані інтерфейси та класи
title: Клас Closure
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Closure

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

## Вступ

Клас, який використовується для створення [анонімних функцій](functions.anonymous.md)

Анонімні функції видають об'єкти цього. Клас отримав методи, що дозволяють контролювати анонімну функцію після її створення.

Крім методів, описаних тут, цей клас також має метод `__invoke`. Цей метод необхідний лише сумісності з іншими класами, у яких реалізований [магічний виклик](language.oop5.magic.md#language.oop5.magic.invoke), оскільки цей метод не використовується під час виклику функції.

## Огляд класів

```classsynopsis

    
     final
     class Closure
     {

    /* Методы */
    
   private __construct()

    public static bind(Closure $closure, ?object $newThis, object|string|null $newScope = "static"): ?Closure
public bindTo(?object $newThis, object|string|null $newScope = "static"): ?Closure
public call(object $newThis, mixed ...$args): mixed
public static fromCallable(callable $callback): Closure

   }
```

## Зміст

-   [Closure::\_\_construct](closure.construct.md) \- Конструктор, який забороняє створення екземпляра
-   [Closure::bind](closure.bind.md)— Дублює замикання із зазначенням конкретного зв'язаного об'єкта та області видимості класу
-   [Closure::bindTo](closure.bindto.md)— Дублює замикання із зазначенням пов'язаного об'єкта та області видимості класу
-   [Closure::call](closure.call.md)— Зв'язує та запускає замикання
-   [Closure::fromCallable](closure.fromcallable.md)— Конвертує callable у замикання
