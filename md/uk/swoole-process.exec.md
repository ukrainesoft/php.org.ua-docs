---
navigation:
  - swoole-process.destruct.md: '« Swoole\\Process::\_\_destruct'
  - swoole-process.exit.md: 'Swoole\\Process::exit »'
  - index.md: PHP Manual
  - class.swoole-process.md: Swoole\\Process
title: 'Swoole\\Process::exec'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Process::exec

(PECL swoole >= 1.9.0)

Swoole\\Process::exec — Виконує системні команди

### Опис

```methodsynopsis
public Swoole\Process::exec(string $exec_file, string $args): ReturnType
```

Процес буде замінено на системний командний процес, але канал до батьківського процесу буде збережено.

### Список параметрів

`exec_file`

`args`

### Значення, що повертаються
