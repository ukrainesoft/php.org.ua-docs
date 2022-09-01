---
navigation:
  - swoole-websocket-server.on.html: '« SwooleWebSocketServer::on'
  - swoole-websocket-server.push.html: 'SwooleWebSocketServer::push »'
  - index.md: PHP Manual
  - class.swoole-websocket-server.html: SwooleWebSocketServer
title: 'SwooleWebSocketServer::pack'
---
# SwooleWebSocketServer::pack

(PECL swoole >= 1.9.0)

SwooleWebSocketServer::pack — Отримання пакета двійкових даних для надсилання в одній групі даних (frame)

### Опис

```methodsynopsis
public static Swoole\WebSocket\Server::pack(    string $data,    string $opcode = ?,    string $finish = ?,    string $mask = ?): binary
```

### Список параметрів

`data`

`opcode`

`finish`

`mask`

### Значення, що повертаються
