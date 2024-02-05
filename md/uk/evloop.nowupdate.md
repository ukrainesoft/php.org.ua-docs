---
navigation:
  - evloop.now.md: '« EvLoop::now'
  - evloop.periodic.md: 'EvLoop::periodic »'
  - index.md: PHP Manual
  - class.evloop.md: EvLoop
title: 'EvLoop::nowUpdate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvLoop::nowUpdate

(PECL ev >= 0.2.0)

EvLoop::nowUpdate — Встановлює поточний час, запитуючи ядро, оновлюючи час, який повертається EvLoop::now у процесі

### Опис

```methodsynopsis
public
   EvLoop::nowUpdate(): void
```

Встановлює поточний час, запитуючи ядро, оновлюючи час, що повертається [EvLoop::now()](evloop.now.md) в процесі. Це дорога операція, яка зазвичай виконується автоматично [EvLoop::run()](evloop.run.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [EvLoop::now()](evloop.now.md) - Повертає поточний "event loop time"
-   [Ev::nowUpdate()](ev.nowupdate.md) \- Встановлює поточний час шляхом запиту до ядра в процесі оновлюючи час, який повертається Ev::now
