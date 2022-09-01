---
navigation:
  - swoole-mysql.getbuffer.html: '« SwooleMySQL::getBuffer'
  - swoole-mysql.query.html: 'SwooleMySQL::query »'
  - index.md: PHP Manual
  - class.swoole-mysql.html: SwooleMySQL
title: 'SwooleMySQL::on'
---
# SwooleMySQL::on

(PECL swoole >= 1.9.0)

SwooleMySQL::on - Реєструє callback-функцію на основі імені події

### Опис

```methodsynopsis
public Swoole\MySQL::on(string $event_name, callable $callback): void
```

Реєструє callback-функцію на основі імені події, на даний момент підтримується лише подія 'close'.

### Список параметрів

`event_name`

`callback`

### Значення, що повертаються
