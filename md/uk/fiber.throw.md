Відновлює виконання файбера за винятком

-   [« Fiber::resume](fiber.resume.md)
    
-   [Fiber::getReturn »](fiber.getreturn.md)
    
-   [PHP Manual](index.md)
    
-   [Fiber](class.fiber.md)
    
-   Відновлює виконання файбера за винятком
    

# Fiber::throw

(PHP 8> = 8.1.0)

Fiber::throw — Відновлює виконання файбера за винятком

### Опис

```methodsynopsis
public Fiber::throw(Throwable $exception): mixed
```

Відновлює виконання файбера, викидаючи цей виняток із поточного виклику [Fiber::suspend()](fiber.suspend.md)

Якщо файбер не призупинено під час виклику методу, буде викинуто помилку [FiberError](class.fibererror.md)

### Список параметрів

`exception`

Виняток, який потрібно передати до файбера з поточного виклику [Fiber::suspend()](fiber.suspend.md)

### Значення, що повертаються

Значення, надане під час першого виклику [Fiber::suspend()](fiber.suspend.md) або **`null`** у разі повернення файбера. Якщо файбер викинув виняток перед призупиненням, його буде викинуто з цього методу.