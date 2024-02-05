---
navigation:
  - evloop.timer.md: '« EvLoop::timer'
  - class.evperiodic.md: EvPeriodic »
  - index.md: PHP Manual
  - class.evloop.md: EvLoop
title: 'EvLoop::verify'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvLoop::verify

(PECL ev >= 0.2.0)

EvLoop::verify — Виконує внутрішні перевірки узгодженості (для налагодження)

### Опис

```methodsynopsis
public
   EvLoop::verify(): void
```

Виконує внутрішні перевірки узгодженості (для налагодження *libev*) і перериває програму, якщо виявлено пошкоджені структури даних.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [Ev::verify()](ev.verify.md) \- Здійснює внутрішню перевірку цілісності (для налагодження)
