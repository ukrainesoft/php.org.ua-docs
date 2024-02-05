---
navigation:
  - swoole-process.freequeue.md: '« Swoole\\Process::freeQueue'
  - swoole-process.name.md: 'Swoole\\Process::name »'
  - index.md: PHP Manual
  - class.swoole-process.md: Swoole\\Process
title: 'Swoole\\Process::kill'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Process::kill

(PECL swoole >= 1.9.0)

Swoole\\Process::kill — Надсилає сигнал дочірньому процесу

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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
