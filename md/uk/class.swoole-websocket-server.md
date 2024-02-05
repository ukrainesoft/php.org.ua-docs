---
navigation:
  - class.swoole-websocket-frame.md: « Swoole\\WebSocket\\Frame
  - swoole-websocket-server.exist.md: 'Swoole\\WebSocket\\Server::exist »'
  - index.md: PHP Manual
  - book.swoole.md: Swoole
title: Клас Swoole\\WebSocket\\Server
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Swoole\\WebSocket\\Server

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

-   [Swoole\\WebSocket\\Server::exist](swoole-websocket-server.exist.md)— Перевіряє, чи є опис файлу
-   [Swoole\\WebSocket\\Server::on](swoole-websocket-server.on.md) \- Зареєструвати callback-функцію події
-   [Swoole\\WebSocket\\Server::pack](swoole-websocket-server.pack.md)— Отримання пакета двійкових даних для надсилання в одній групі даних (frame)
-   [Swoole\\WebSocket\\Server::push](swoole-websocket-server.push.md)— Надіслати дані віддаленому клієнту
-   [Swoole\\WebSocket\\Server::unpack](swoole-websocket-server.unpack.md) \- Розпакувати двійкові дані, отримані від клієнта
