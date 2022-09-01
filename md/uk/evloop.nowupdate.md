---
navigation:
  - evloop.now.html: '« EvLoop::now'
  - evloop.periodic.html: 'EvLoop::periodic »'
  - index.html: PHP Manual
  - class.evloop.html: EvLoop
title: 'EvLoop::nowUpdate'
---
# EvLoop::nowUpdate

(PECL ev >= 0.2.0)

EvLoop::nowUpdate — Встановлює поточний час, запитуючи ядро, оновлюючи час, що повертається EvLoop::now у процесі

### Опис

```methodsynopsis
public
   EvLoop::nowUpdate(): void
```

Встановлює поточний час, запитуючи ядро, оновлюючи час, що повертається [EvLoop::now()](evloop.now.html) в процесі. Це дорога операція, яка зазвичай виконується автоматично [EvLoop::run()](evloop.run.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [EvLoop::now()](evloop.now.html) - Повертає поточний "event loop time"
-   [Ev::nowUpdate()](ev.nowupdate.html) - Встановлює поточний час шляхом запиту до ядра в процесі оновлюючи час, який повертається Ev::now
