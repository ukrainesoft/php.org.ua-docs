Клас Closure

-   [« Serializable::unserialize](serializable.unserialize.html)
    
-   [Closure::construct »](closure.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Вбудовані інтерфейси та класи](reserved.interfaces.html)
    
-   Клас Closure
    

# Клас Closure

(PHP 5> = 5.3.0, PHP 7, PHP 8)

## Вступ

Клас, який використовується для створення [анонимных функций](functions.anonymous.html)

Анонімні функції видають об'єкти цього. Клас отримав методи, що дозволяють контролювати анонімну функцію після її створення.

Крім методів, описаних тут, цей клас також має метод `__invoke`. Цей метод необхідний лише сумісності з іншими класами, у яких реалізований [магічний виклик](language.oop5.magic.html#language.oop5.magic.invoke), оскільки цей метод не використовується під час виклику функції.

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

-   [Closure::construct](closure.construct.html) - Конструктор, який забороняє створення екземпляра
-   [Closure::bind](closure.bind.html) — Дублює замикання із зазначенням конкретного зв'язаного об'єкта та області видимості класу
-   [Closure::bindTo](closure.bindto.html) — Дублює замикання із зазначенням пов'язаного об'єкта та області видимості класу
-   [Closure::call](closure.call.html) — Зв'язує та запускає замикання
-   [Closure::fromCallable](closure.fromcallable.html) — Конвертує callable у замикання