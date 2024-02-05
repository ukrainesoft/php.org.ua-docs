---
navigation:
  - evstat.createstopped.md: '« EvStat::createStopped'
  - evstat.set.md: 'EvStat::set »'
  - index.md: PHP Manual
  - class.evstat.md: EvStat
title: 'EvStat::prev'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvStat::prev

(PECL ev >= 0.2.0)

EvStat::prev — Повертає попередній набір значень, які повертаються EvStat::attr

### Опис

```methodsynopsis
public
   EvStat::prev(): void
```

Як і [EvStat::attr()](evstat.attr.md) але повертає попередній набір значень.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив з тією ж структурою, що і масив, що повертається [EvStat::attr()](evstat.attr.md). Масив містить попередній набір значень.

### Дивіться також

-   [EvStat::attr()](evstat.attr.md) \- Повертає значення, нещодавно виявлені Ev
-   [EvStat::stat()](evstat.stat.md) \- Ініціює виклик статистики
