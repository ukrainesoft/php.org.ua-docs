Відновлює виконання файбера зі значенням

-   [« Fiber::start](fiber.start.html)
    
-   [Fiber::throw »](fiber.throw.html)
    
-   [PHP Manual](index.html)
    
-   [Fiber](class.fiber.html)
    
-   Відновлює виконання файбера зі значенням
    

# Fiber::resume

(PHP 8> = 8.1.0)

Fiber::resume — Відновлює виконання файбера зі значенням

### Опис

```methodsynopsis
public Fiber::resume(mixed $value = null): mixed
```

Відновлює файл, використовуючи задане значення в результаті поточного виклику [Fiber::suspend()](fiber.suspend.html)

Якщо файбер не призупинено під час виклику методу, буде викинуто помилку [FiberError](class.fibererror.html)

### Список параметрів

`value`

Значення відновлення файбера. Значення буде повертати значення поточного виклику [Fiber::suspend()](fiber.suspend.html)

### Значення, що повертаються

Значення для наступного виклику [Fiber::suspend()](fiber.suspend.html) або **`null`** у разі повернення файбера. Якщо файбер викинув виняток перед призупиненням, його буде викинуто з цього методу.