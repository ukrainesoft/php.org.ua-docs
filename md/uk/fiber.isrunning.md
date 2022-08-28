Визначає, чи працює файбер

-   [« Fiber::isSuspended](fiber.issuspended.html)
    
-   [Fiber::isTerminated »](fiber.isterminated.html)
    
-   [PHP Manual](index.html)
    
-   [Fiber](class.fiber.html)
    
-   Визначає, чи працює файбер
    

# Fiber::isRunning

(PHP 8> = 8.1.0)

Fiber::isRunning — Визначає, чи працює файбер

### Опис

```methodsynopsis
public Fiber::isRunning(): bool
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** тільки якщо файбер працює. Файбер вважається працюючим після виклику [Fiber::start()](fiber.start.html) [Fiber::resume()](fiber.resume.html) або [Fiber::throw()](fiber.throw.html), який ще не повернуто. Повертає **`false`**якщо файбер не працює.