---
navigation:
  - parallel-events.setblocking.html: '« parallelEvents::setBlocking'
  - parallel-events.setinput.html: 'parallelEvents::setInput »'
  - index.html: PHP Manual
  - class.parallel-events.html: parallelEvents
title: 'parallelEvents::setTimeout'
---
# parallelEvents::setTimeout

parallelEvents::setTimeout — Поведінка

### Опис

За замовчуванням при опитуванні подій відбувається блокування (на рівні PHP), доки не буде повернена перша подія: встановлення часу очікування призводить до викидання виключення при перевищенні часу очікування.

Відрізняється від встановлення режиму блокування в **`false`** за допомогою [parallelEvents::setBlocking()](parallel-events.setblocking.html), що не викидає виняток.

```methodsynopsis
public parallel\Events::setTimeout(int $timeout): void
```

Встановлює час очікування у мікросекундах

### Помилки

**Увага**

Викидає parallelEventsError, якщо цикл не блокується.
