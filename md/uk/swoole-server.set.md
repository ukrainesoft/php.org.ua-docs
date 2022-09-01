---
navigation:
  - swoole-server.sendwait.html: '« SwooleServer::sendwait'
  - swoole-server.shutdown.html: 'SwooleServer::shutdown »'
  - index.html: PHP Manual
  - class.swoole-server.html: SwooleServer
title: 'SwooleServer::set'
---
# SwooleServer::set

(PECL swoole >= 1.9.0)

SwooleServer::set — Встановлює налаштування часу виконання сервера swoole

### Опис

```methodsynopsis
public Swoole\Server::set(array $settings): ReturnType
```

Встановлює налаштування часу виконання сервера swoole. Доступ до налаштувань можна отримати за допомогою $server->setting після запуску сервера swoole.

### Список параметрів

`settings`

### Значення, що повертаються
