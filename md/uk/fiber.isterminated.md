Визначає, чи завершено файбер

-   [« Fiber::isRunning](fiber.isrunning.html)
    
-   [Fiber::suspend »](fiber.suspend.html)
    
-   [PHP Manual](index.html)
    
-   [Fiber](class.fiber.html)
    
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