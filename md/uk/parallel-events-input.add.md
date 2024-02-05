---
navigation:
  - class.parallel-events-input.md: « parallel\\Events\\Input
  - parallel-events-input.clear.md: 'parallel\\Events\\Input::clear »'
  - index.md: PHP Manual
  - class.parallel-events-input.md: parallel\\Events\\Input
title: 'parallel\\Events\\Input::add'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# parallel\\Events\\Input::add

(0.9.0)

parallel\\Events\\Input::add — Вхід

### Опис

```methodsynopsis
public parallel\Events\Input::add(string $target, mixed $value): void
```

Встановлює вхід для заданої мети

### Помилки

**Увага**

Викидає parallel\\Events\\Input\\Error\\Existence, якщо вхід до мети вже існує.

**Увага**

Викидає parallel\\Events\\Input\\Error\\IllegalValue, если значение недопустимо (object,**`null`**
