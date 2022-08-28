Зупиняє виконання поточного файбера

-   [« Fiber::isTerminated](fiber.isterminated.html)
    
-   [Fiber::getCurrent »](fiber.getcurrent.html)
    
-   [PHP Manual](index.html)
    
-   [Fiber](class.fiber.html)
    
-   Зупиняє виконання поточного файбера
    

# Fiber::suspend

(PHP 8> = 8.1.0)

Fiber::suspend — Зупиняє виконання поточного файбера

### Опис

```methodsynopsis
public static Fiber::suspend(mixed $value = null): mixed
```

Зупиняє виконання поточного файбера. Значення, надане цим методом, буде повернено з виклику [Fiber::start()](fiber.start.html) [Fiber::resume()](fiber.resume.html) або [Fiber::throw()](fiber.throw.html), що переключив виконання поточного файбера.

Коли виконання файбера відновлюється, метод повертає значення, надане в [Fiber::resume()](fiber.resume.html). Якщо виконання файбера відновлюється за допомогою Fiber::throw, виняток, переданий цьому методу, буде викинуто під час виклику методу.

Якщо цей метод викликається ззовні файбера, буде викинуто помилку [FiberError](class.fibererror.html)

### Список параметрів

`value`

Значення, що повертається під час виклику [Fiber::start()](fiber.start.html) [Fiber::resume()](fiber.resume.html) або [Fiber::throw()](fiber.throw.html), що перемикають виконання поточного файбера.

### Значення, що повертаються

Значення, надане [Fiber::resume()](fiber.resume.html)