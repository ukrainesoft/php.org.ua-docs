---
navigation:
  - ui-executor.onexecute.md: '« UIExecutor::onExecute'
  - class.ui-controls-tab.md: ОЙControlsTab »
  - index.md: PHP Manual
  - class.ui-executor.md: ОЙExecutor
title: 'ОЙExecutor::setInterval'
---
# ОЙExecutor::setInterval

(UI 2.0.0)

ОЙExecutor::setInterval — Керування інтервалом

### Опис

```methodsynopsis
public UI\Executor::setInterval(int $microseconds): bool
```

```methodsynopsis
public UI\Executor::setInterval(int $seconds, int $microseconds): bool
```

Встановить новий інтервал. Інтервал 0 припиняє виконання виконавцем доти, доки не буде встановлено новий інтервал

### Список параметрів

`seconds`

`microseconds`

### Значення, що повертаються

Індикатор успішності виконання
