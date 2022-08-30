Відновлює виконання файбера зі значенням

-   [« Fiber::start](fiber.start.md)
    
-   [Fiber::throw »](fiber.throw.md)
    
-   [PHP Manual](index.md)
    
-   [Fiber](class.fiber.md)
    
-   Відновлює виконання файбера зі значенням
    

# Fiber::resume

(PHP 8> = 8.1.0)

Fiber::resume — Відновлює виконання файбера зі значенням

### Опис

```methodsynopsis
public Fiber::resume(mixed $value = null): mixed
```

Відновлює файл, використовуючи задане значення в результаті поточного виклику [Fiber::suspend()](fiber.suspend.md)

Якщо файбер не призупинено під час виклику методу, буде викинуто помилку [FiberError](class.fibererror.md)

### Список параметрів

`value`

Значення відновлення файбера. Значення буде повертати значення поточного виклику [Fiber::suspend()](fiber.suspend.md)

### Значення, що повертаються

Значення для наступного виклику [Fiber::suspend()](fiber.suspend.md) або **`null`** у разі повернення файбера. Якщо файбер викинув виняток перед призупиненням, його буде викинуто з цього методу.