Створює канал Swoole

-   [« Swoole\\Channel](class.swoole-channel.html)
    
-   [Swoole\\Channel::\_\_destruct »](swoole-channel.destruct.html)
    
-   [PHP Manual](index.html)
    
-   [Swoole\\Channel](class.swoole-channel.html)
    
-   Створює канал Swoole
    

# SwooleChannel::construct

(PECL swoole >= 1.9.0)

SwooleChannel::construct — Створює канал Swoole

### Опис

public **SwooleChannel::construct**(string `$size`

Канал Swoole - це структура даних у пам'яті, яка працює як Chan в Golang, реалізована на основі пам'яті, що розділяється, і мьютексів. Може використовуватись як високопродуктивна черга повідомлень у пам'яті. Створення каналу Swoole із фіксованим розміром. Мінімальний розмір каналу Swoole складає 64 КБ. Викинуть винятки, якщо недостатньо пам'яті.

### Список параметрів

`size`

Розмір каналу Swoole.