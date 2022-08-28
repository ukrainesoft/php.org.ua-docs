Створює синхронний або асинхронний TCP/UDP клієнт Swoole за допомогою SSL або без нього

-   [« Swoole\\Client::connect](swoole-client.connect.html)
    
-   [Swoole\\Client::\_\_destruct »](swoole-client.destruct.html)
    
-   [PHP Manual](index.html)
    
-   [Swoole\\Client](class.swoole-client.html)
    
-   Створює синхронний або асинхронний TCP/UDP клієнт Swoole за допомогою SSL або без нього
    

# SwooleClient::construct

(PECL swoole >= 1.9.0)

SwooleClient::construct — Створює синхронний або асинхронний TCP/UDP клієнт Swoole із підтримкою SSL або без нього

### Опис

public **SwooleClient::construct**(int `$sock_type`, int `$is_async`

### Список параметрів

`sock_type`

Тип сокету: SWOOLETCP, SWOOLEUDP, SWOOLEASYNC, SWOOLESSL, SWOOLEKEEP.

`is_async`

Синхронний чи асинхронний клієнт.