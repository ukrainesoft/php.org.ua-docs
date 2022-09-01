---
navigation:
  - swoole-process.freequeue.html: '« SwooleProcess::freeQueue'
  - swoole-process.name.html: 'SwooleProcess::name »'
  - index.html: PHP Manual
  - class.swoole-process.html: SwooleProcess
title: 'SwooleProcess::kill'
---
# SwooleProcess::kill

(PECL swoole >= 1.9.0)

SwooleProcess::kill — Надсилає сигнал дочірньому процесу

### Опис

```methodsynopsis
public static Swoole\Process::kill(int $pid, int $signal_no = ?): bool
```

Надсилає сигнал дочірньому процесу.

### Список параметрів

`pid`

Ідентифікатор процесу

`signal_no`

Сигнал до відправлення

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
