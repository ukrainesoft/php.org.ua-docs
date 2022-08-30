Створює новий екземпляр Fiber

-   [« Fiber](class.fiber.md)
    
-   [Fiber::start »](fiber.start.md)
    
-   [PHP Manual](index.md)
    
-   [Fiber](class.fiber.md)
    
-   Створює новий екземпляр Fiber
    

# Fiber::construct

(PHP 8> = 8.1.0)

Fiber::construct - Створює новий екземпляр Fiber

### Опис

public **Fiber::construct**[callable](language.types.callable.md) `$callback`

### Список параметрів

`callback`

[callable](language.types.callable.md)функція виклику під час запуску файбера. Аргументи для [Fiber::start()](fiber.start.md) будуть надається як аргументи для даного викликаного об'єкта.