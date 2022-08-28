Отримує номер рядка поточної точки виконання

-   [« ReflectionFiber::getExecutingFile](reflectionfiber.getexecutingfile.html)
    
-   [ReflectionFiber::getFiber »](reflectionfiber.getfiber.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionFiber](class.reflectionfiber.html)
    
-   Отримує номер рядка поточної точки виконання
    

# ReflectionFiber::getExecutingLine

(PHP 8> = 8.1.0)

ReflectionFiber::getExecutingLine — Отримує номер рядка поточної точки виконання

### Опис

```methodsynopsis
public ReflectionFiber::getExecutingLine(): int
```

Повертає номер рядка поточної точки виконання у відбитому класі [Fiber](class.fiber.html). Якщо файбер не було запущено або завершено, видається помилка [Error](class.error.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Номер рядка поточної точки виконання файбера.