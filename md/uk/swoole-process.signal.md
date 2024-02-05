---
navigation:
  - swoole-process.read.md: '« Swoole\\Process::read'
  - swoole-process.start.md: 'Swoole\\Process::start »'
  - index.md: PHP Manual
  - class.swoole-process.md: Swoole\\Process
title: 'Swoole\\Process::signal'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Process::signal

(PECL swoole >= 1.9.0)

Swoole\\Process::signal — Надсилає сигнал дочірнім процесам

### Опис

```methodsynopsis
public static Swoole\Process::signal(string $signal_no, callable $callback): void
```

### Список параметрів

`signal_no`

`callback`

### Значення, що повертаються

У разі успішного відправлення сигналу, повертає TRUE, інакше повертає FALSE.
