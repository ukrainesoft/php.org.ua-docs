---
navigation:
  - evstat.set.md: '« EvStat::set'
  - class.evtimer.md: EvTimer »
  - index.md: PHP Manual
  - class.evstat.md: EvStat
title: 'Евстат::стати'
---
# Евстат::стати

(PECL ev >= 0.2.0)

EvStat::stat — Ініціює виклик статистики

### Опис

```methodsynopsis
public
   EvStat::stat(): bool
```

Ініціює виклик статистики (оновлює внутрішній кеш). Визначає (використовуючи `lstat`) path, вказаний у спостерігачі, та встановлює знайдені значення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо path існує. В іншому випадку **`false`**

### Дивіться також

-   [EvStat::attr()](evstat.attr.md) - Повертає значення, нещодавно виявлені Ev
-   [EvStat::prev()](evstat.prev.md) - Повертає попередній набір значень, які повертаються EvStat::attr
