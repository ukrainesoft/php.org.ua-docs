---
navigation:
  - swoole-process.destruct.html: '« SwooleProcess::destruct'
  - swoole-process.exit.html: 'SwooleProcess::exit »'
  - index.md: PHP Manual
  - class.swoole-process.html: SwooleProcess
title: 'SwooleProcess::exec'
---
# SwooleProcess::exec

(PECL swoole >= 1.9.0)

SwooleProcess::exec — Виконує системні команди

### Опис

```methodsynopsis
public Swoole\Process::exec(string $exec_file, string $args): ReturnType
```

Процес буде замінено на системний командний процес, на канал до батьківського процесу буде збережено.

### Список параметрів

`exec_file`

`args`

### Значення, що повертаються
