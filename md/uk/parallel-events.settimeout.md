---
navigation:
  - parallel-events.setblocking.md: '« parallel\\Events::setBlocking'
  - parallel-events.setinput.md: 'parallel\\Events::setInput »'
  - index.md: PHP Manual
  - class.parallel-events.md: parallel\\Events
title: 'parallel\\Events::setTimeout'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# parallel\\Events::setTimeout

(0.9.0)

parallel\\Events::setTimeout — Поведінка

### Опис

За замовчуванням при опитуванні подій відбувається блокування (на рівні PHP) доти, доки не буде повернена перша подія: встановлення часу очікування призводить до викидання винятку при перевищенні часу очікування.

Отличается от установки режима блокировки в\*\*`false`\*\* за допомогою [parallel\\Events::setBlocking()](parallel-events.setblocking.md), що не викидає виняток.

```methodsynopsis
public parallel\Events::setTimeout(int $timeout): void
```

Встановлює час очікування у мікросекундах

### Помилки

**Увага**

Викидає parallel\\Events\\Error, якщо цикл не блокується.
