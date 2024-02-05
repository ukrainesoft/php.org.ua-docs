---
navigation:
  - swoole-client.connect.md: '« Swoole\\Client::connect'
  - swoole-client.destruct.md: 'Swoole\\Client::\_\_destruct »'
  - index.md: PHP Manual
  - class.swoole-client.md: Swoole\\Client
title: 'Swoole\\Client::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Client::\_\_construct

(PECL swoole >= 1.9.0)

Swoole\\Client::\_\_construct — Створює синхронний або асинхронний TCP/UDP клієнт Swoole із підтримкою SSL або без нього

### Опис

public**Swoole\\Client::\_\_construct**(int`$sock_type`, int`$is_async`

### Список параметрів

`sock_type`

Тип сокету: SWOOLE\_TCP, SWOOLE\_UDP, SWOOLE\_ASYNC, SWOOLE\_SSL, SWOOLE\_KEEP.

`is_async`

Синхронний чи асинхронний клієнт.
