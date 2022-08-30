Визначає, чи завершено файбер

-   [« Fiber::isRunning](fiber.isrunning.md)
    
-   [Fiber::suspend »](fiber.suspend.md)
    
-   [PHP Manual](index.md)
    
-   [Fiber](class.fiber.md)
    
-   Визначає, чи завершено файбер
    

# Fiber::isTerminated

(PHP 8> = 8.1.0)

Fiber::isTerminated — Визначає, чи файбер завершено.

### Опис

```methodsynopsis
public Fiber::isTerminated(): bool
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** тільки після того, як файбер завершився, або шляхом повернення, або викинувши виняток, інакше повертає **`false`**