---
navigation:
  - parallel-events.remove.html: '« parallelEvents::remove'
  - class.parallel-events-input.html: parallelEventsInput »
  - index.md: PHP Manual
  - class.parallel-events.html: parallelEvents
title: 'parallelEvents::poll'
---
# parallelEvents::poll

parallelEvents::poll — Опитування

### Опис

```methodsynopsis
public parallel\Events::poll(): ?parallel\Events\Event
```

Опитує для наступної події

### Значення, що повертаються

Якщо цілей не залишилося, повертається **`null`**

Якщо це буде неблокуючий цикл і відбудеться блокування, буде повернено значення **`null`**

В іншому випадку [parallelEventsEvent](class.parallel-events-event.html) повертає опис події.

### Помилки

**Увага**

Викидає parallelEventsErrorTimeout, якщо час очікування використано та досягнуто.
