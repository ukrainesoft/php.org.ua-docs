Отримує значення, яке повертається файбером

-   [« Fiber::throw](fiber.throw.html)
    
-   [Fiber::isStarted »](fiber.isstarted.html)
    
-   [PHP Manual](index.html)
    
-   [Fiber](class.fiber.html)
    
-   Отримує значення, яке повертається файбером
    

# Fiber::getReturn

(PHP 8> = 8.1.0)

Fiber::getReturn — Отримує значення, яке повертається файбером

### Опис

```methodsynopsis
public Fiber::getReturn(): mixed
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає значення, що повертається [callable](language.types.callable.html)функцією, наданою в [Fiber::\_\_construct()](fiber.construct.html). Якщо файбер не повернув значення, або тому, що він не був запущений, або не був завершений, або викинув виняток, буде викинуто виняток [FiberError](class.fibererror.html)