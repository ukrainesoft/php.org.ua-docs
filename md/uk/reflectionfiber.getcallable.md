Отримує об'єкт, що використовується для створення файбера

-   [« ReflectionFiber::\_\_construct](reflectionfiber.construct.html)
    
-   [ReflectionFiber::getExecutingFile »](reflectionfiber.getexecutingfile.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionFiber](class.reflectionfiber.html)
    
-   Отримує об'єкт, що використовується для створення файбера
    

# ReflectionFiber::getCallable

(PHP 8> = 8.1.0)

ReflectionFiber::getCallable — Отримує об'єкт, що викликається, що використовується для створення файбера

### Опис

```methodsynopsis
public ReflectionFiber::getCallable(): callable
```

Повертає об'єкт, що використовується для створення [Fiber](class.fiber.html). Якщо файбер завершено, видається помилка [Error](class.error.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт, що використовується для створення [Fiber](class.fiber.html)