---
navigation:
  - parallel-events.setblocking.md: '« parallelEvents::setBlocking'
  - parallel-events.setinput.md: 'parallelEvents::setInput »'
  - index.md: PHP Manual
  - class.parallel-events.md: parallelEvents
title: 'parallelEvents::setTimeout'
---
# parallelEvents::setTimeout

parallelEvents::setTimeout — Поведінка

### Опис

За замовчуванням при опитуванні подій відбувається блокування (на рівні PHP), доки не буде повернена перша подія: встановлення часу очікування призводить до викидання виключення при перевищенні часу очікування.

Відрізняється від встановлення режиму блокування в **`false`** за допомогою [parallelEvents::setBlocking()](parallel-events.setblocking.md), що не викидає виняток.

```methodsynopsis
public parallel\Events::setTimeout(int $timeout): void
```

Встановлює час очікування у мікросекундах

### Помилки

**Увага**

Викидає parallelEventsError, якщо цикл не блокується.
