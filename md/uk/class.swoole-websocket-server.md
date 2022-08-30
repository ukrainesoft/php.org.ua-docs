Клас SwooleWebSocketServer

-   [« SwooleWebSocketFrame](class.swoole-websocket-frame.html)
    
-   [SwooleWebSocketServer::exist »](swoole-websocket-server.exist.html)
    
-   [PHP Manual](index.html)
    
-   [Swoole](book.swoole.html)
    
-   Клас SwooleWebSocketServer
    

# Клас SwooleWebSocketServer

(PECL swoole >= 1.9.0)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class Swoole\WebSocket\Server
     

     
      extends
       Swoole\Http\Server
     
     {


    /* Методы */
    
   public exist(int $fd): bool
public on(string $event_name, callable $callback): ReturnType
public static pack(    string $data,    string $opcode = ?,    string $finish = ?,    string $mask = ?): binary
public push(    string $fd,    string $data,    string $opcode = ?,    string $finish = ?): void
public static unpack(binary $data): string


    /* Наследуемые методы */
    public Swoole\Http\Server::on(string $event_name, callable $callback): void
public Swoole\Http\Server::start(): void


   }
```

## Зміст

-   [SwooleWebSocketServer::exist](swoole-websocket-server.exist.html) — Перевіряє, чи є опис файлу
-   [SwooleWebSocketServer::on](swoole-websocket-server.on.html) - Зареєструвати callback-функцію події
-   [SwooleWebSocketServer::pack](swoole-websocket-server.pack.html) — Отримання пакета двійкових даних для надсилання в одній групі даних (frame)
-   [SwooleWebSocketServer::push](swoole-websocket-server.push.html) — Надіслати дані віддаленому клієнту
-   [SwooleWebSocketServer::unpack](swoole-websocket-server.unpack.html) - Розпакувати двійкові дані, отримані від клієнта