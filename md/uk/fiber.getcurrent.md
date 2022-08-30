Отримує поточний екземпляр Fiber

-   [« Fiber::suspend](fiber.suspend.md)
    
-   [WeakReference »](class.weakreference.md)
    
-   [PHP Manual](index.md)
    
-   [Fiber](class.fiber.md)
    
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

Повертає екземпляр, що виконується в даний момент. [Fiber](class.fiber.md) або \*\*`null`\*\*якщо метод викликається ззовні файбера.