Отримує ім'я файлу поточної точки виконання

-   [« ReflectionFiber::getCallable](reflectionfiber.getcallable.html)
    
-   [ReflectionFiber::getExecutingLine »](reflectionfiber.getexecutingline.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionFiber](class.reflectionfiber.html)
    
-   Отримує ім'я файлу поточної точки виконання
    

# ReflectionFiber::getExecutingFile

(PHP 8> = 8.1.0)

ReflectionFiber::getExecutingFile — Отримує ім'я файлу поточної точки виконання

### Опис

```methodsynopsis
public ReflectionFiber::getExecutingFile(): string
```

Повертає повний шлях та ім'я файлу поточної точки виконання у відображеному класі [Fiber](class.fiber.html). Якщо файбер не було запущено або завершено, видається помилка [Error](class.error.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повний шлях та ім'я файлу відбитого файбера.