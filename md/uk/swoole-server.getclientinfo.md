---
navigation:
  - swoole-server.finish.md: '« Swoole\\Server::finish'
  - swoole-server.getclientlist.md: 'Swoole\\Server::getClientList »'
  - index.md: PHP Manual
  - class.swoole-server.md: Swoole\\Server
title: 'Swoole\\Server::getClientInfo'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Server::getClientInfo

(PECL swoole >= 1.9.0)

Swoole\\Server::getClientInfo — Отримує інформацію про з'єднання з описом файлу

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
