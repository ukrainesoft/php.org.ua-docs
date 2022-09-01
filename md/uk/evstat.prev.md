---
navigation:
  - evstat.createstopped.html: '« EvStat::createStopped'
  - evstat.set.html: 'EvStat::set »'
  - index.html: PHP Manual
  - class.evstat.html: EvStat
title: 'EvStat::prev'
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

-   [EvStat::attr()](evstat.attr.md) - Повертає значення, нещодавно виявлені Ev
-   [EvStat::stat()](evstat.stat.md) - Ініціює виклик статистики
