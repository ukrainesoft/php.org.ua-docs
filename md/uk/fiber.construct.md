Створює новий екземпляр Fiber

-   [« Fiber](class.fiber.html)
    
-   [Fiber::start »](fiber.start.html)
    
-   [PHP Manual](index.html)
    
-   [Fiber](class.fiber.html)
    
-   Створює новий екземпляр Fiber
    

# Fiber::construct

(PHP 8> = 8.1.0)

Fiber::construct - Створює новий екземпляр Fiber

### Опис

public **Fiber::construct**[callable](language.types.callable.html) `$callback`

### Список параметрів

`callback`

[callable](language.types.callable.html)функція виклику під час запуску файбера. Аргументи для [Fiber::start()](fiber.start.html) будуть надається як аргументи для даного викликаного об'єкта.