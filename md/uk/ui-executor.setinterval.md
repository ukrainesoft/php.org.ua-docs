---
navigation:
  - ui-executor.onexecute.md: '« UI\\Executor::onExecute'
  - class.ui-controls-tab.md: UI\\Controls\\Tab »
  - index.md: PHP Manual
  - class.ui-executor.md: UI\\Executor
title: 'UI\\Executor::setInterval'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# UI\\Executor::setInterval

(UI 2.0.0)

UI\\Executor::setInterval — Керування інтервалом

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
