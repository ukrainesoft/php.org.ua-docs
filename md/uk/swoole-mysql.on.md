---
navigation:
  - swoole-mysql.getbuffer.md: '« Swoole\\MySQL::getBuffer'
  - swoole-mysql.query.md: 'Swoole\\MySQL::query »'
  - index.md: PHP Manual
  - class.swoole-mysql.md: Swoole\\MySQL
title: 'Swoole\\MySQL::on'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\MySQL::on

(PECL swoole >= 1.9.0)

Swoole\\MySQL::on - Реєструє callback-функцію на основі імені події

### Опис

```methodsynopsis
public Swoole\MySQL::on(string $event_name, callable $callback): void
```

Реєструє callback-функцію з урахуванням імені події, на даний момент підтримується лише подія 'close'.

### Список параметрів

`event_name`

`callback`

### Значення, що повертаються
