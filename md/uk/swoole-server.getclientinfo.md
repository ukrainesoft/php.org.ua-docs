Отримує інформацію про з'єднання з описом файлу

-   [« SwooleServer::finish](swoole-server.finish.html)
    
-   [SwooleServer::getClientList »](swoole-server.getclientlist.html)
    
-   [PHP Manual](index.html)
    
-   [SwooleServer](class.swoole-server.html)
    
-   Отримує інформацію про з'єднання з описом файлу
    

# SwooleServer::getClientInfo

(PECL swoole >= 1.9.0)

SwooleServer::getClientInfo — Отримує інформацію про з'єднання з описом файлу

### Опис

```methodsynopsis
public Swoole\Server::getClientInfo(int $fd, int $reactor_id = ?, bool $ignore_error = ?): array
```

### Список параметрів

`fd`

Дескриптор файлу

`reactor_id`

Ідентифікатор потоку Reactor, у якому виконується з'єднання.

`ignore_error`

Чи слід ігнорувати помилки. Якщо встановлено значення true, інформацію про з'єднання буде повернуто, навіть якщо з'єднання буде закрито.

### Значення, що повертаються