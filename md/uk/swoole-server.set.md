---
navigation:
  - swoole-server.sendwait.md: '« Swoole\\Server::sendwait'
  - swoole-server.shutdown.md: 'Swoole\\Server::shutdown »'
  - index.md: PHP Manual
  - class.swoole-server.md: Swoole\\Server
title: 'Swoole\\Server::set'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Server::set

(PECL swoole >= 1.9.0)

Swoole\\Server::set — Встановлює налаштування часу виконання сервера swoole

### Опис

```methodsynopsis
public Swoole\Server::set(array $settings): ReturnType
```

Встановлює налаштування часу виконання сервера swoole. Доступ до налаштувань можна отримати за допомогою $server->setting після запуску сервера swoole.

### Список параметрів

`settings`

### Значення, що повертаються
