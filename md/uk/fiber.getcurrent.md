Отримує поточний екземпляр Fiber

-   [« Fiber::suspend](fiber.suspend.html)
    
-   [WeakReference »](class.weakreference.html)
    
-   [PHP Manual](index.html)
    
-   [Fiber](class.fiber.html)
    
-   Отримує поточний екземпляр Fiber
    

# Fiber::getCurrent

(PHP 8> = 8.1.0)

Fiber::getCurrent — Отримує поточний екземпляр Fiber

### Опис

```methodsynopsis
public static Fiber::getCurrent(): ?Fiber
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає екземпляр, що виконується в даний момент. [Fiber](class.fiber.html) або \*\*`null`\*\*якщо метод викликається ззовні файбера.