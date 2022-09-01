---
navigation:
  - swoole-client.connect.html: '« SwooleClient::connect'
  - swoole-client.destruct.html: 'SwooleClient::destruct »'
  - index.md: PHP Manual
  - class.swoole-client.html: SwooleClient
title: 'SwooleClient::construct'
---
# SwooleClient::construct

(PECL swoole >= 1.9.0)

SwooleClient::construct — Створює синхронний або асинхронний TCP/UDP клієнт Swoole із підтримкою SSL або без нього

### Опис

public **SwooleClient::construct**(int `$sock_type`, int `$is_async`

### Список параметрів

`sock_type`

Тип сокету: SWOOLETCP, SWOOLEUDP, SWOOLEASYNC, SWOOLESSL, SWOOLEKEEP.

`is_async`

Синхронний чи асинхронний клієнт.
