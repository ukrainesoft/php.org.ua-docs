---
navigation:
  - swoole-server.finish.html: '« SwooleServer::finish'
  - swoole-server.getclientlist.html: 'SwooleServer::getClientList »'
  - index.md: PHP Manual
  - class.swoole-server.html: SwooleServer
title: 'SwooleServer::getClientInfo'
---
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
