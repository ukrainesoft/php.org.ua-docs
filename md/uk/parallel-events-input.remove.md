---
navigation:
  - parallel-events-input.clear.md: '« parallel\\Events\\Input::clear'
  - class.parallel-events-event.md: parallel\\Events\\Event »
  - index.md: PHP Manual
  - class.parallel-events-input.md: parallel\\Events\\Input
title: 'parallel\\Events\\Input::remove'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# parallel\\Events\\Input::remove

(0.9.0)

parallel\\Events\\Input::remove — Вхід

### Опис

```methodsynopsis
public parallel\Events\Input::remove(string $target): void
```

Видаляє вхід для цієї мети

### Помилки

**Увага**

Викидає parallel\\Events\\Input\\Error\\Existence, якщо вхід до мети не існує.
