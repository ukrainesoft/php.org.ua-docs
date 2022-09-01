---
navigation:
  - swoole-process.read.html: '« SwooleProcess::read'
  - swoole-process.start.html: 'SwooleProcess::start »'
  - index.md: PHP Manual
  - class.swoole-process.html: SwooleProcess
title: 'SwooleProcess::signal'
---
# SwooleProcess::signal

(PECL swoole >= 1.9.0)

SwooleProcess::signal — Надсилає сигнал дочірнім процесам

### Опис

```methodsynopsis
public static Swoole\Process::signal(string $signal_no, callable $callback): void
```

### Список параметрів

`signal_no`

`callback`

### Значення, що повертаються

У разі успішного відправлення сигналу, повертає TRUE, інакше повертає FALSE.
