---
navigation:
  - parallel-events.remove.md: '« parallel\\Events::remove'
  - class.parallel-events-input.md: parallel\\Events\\Input »
  - index.md: PHP Manual
  - class.parallel-events.md: parallel\\Events
title: 'parallel\\Events::poll'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# parallel\\Events::poll

(0.9.0)

parallel\\Events::poll — Опитування

### Опис

```methodsynopsis
public parallel\Events::poll(): ?parallel\Events\Event
```

Опитує для наступної події

### Значення, що повертаються

Якщо цілей не залишилося, повертається **`null`**

Якщо це буде неблокуючий цикл і відбудеться блокування, буде повернено значення **`null`**

В іншому випадку [parallel\\Events\\Event](class.parallel-events-event.md) повертає опис події.

### Помилки

**Увага**

Викидає parallel\\Events\\Error\\Timeout, якщо час очікування використано та досягнуто.
