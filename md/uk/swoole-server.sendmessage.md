---
navigation:
  - swoole-server.sendfile.html: '« SwooleServer::sendfile'
  - swoole-server.sendto.html: 'SwooleServer::sendto »'
  - index.html: PHP Manual
  - class.swoole-server.html: SwooleServer
title: 'SwooleServer::sendMessage'
---
# SwooleServer::sendMessage

(PECL swoole >= 1.9.0)

SwooleServer::sendMessage — Надсилає повідомлення робочим процесам за ідентифікатором

### Опис

```methodsynopsis
public Swoole\Server::sendMessage(int $worker_id, string $data): bool
```

### Список параметрів

`dst_worker_id`

`data`

### Значення, що повертаються
