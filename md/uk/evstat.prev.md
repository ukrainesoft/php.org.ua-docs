Повертає попередній набір значень, які повертаються EvStat::attr

-   [« EvStat::createStopped](evstat.createstopped.html)
    
-   [EvStat::set »](evstat.set.html)
    
-   [PHP Manual](index.html)
    
-   [EvStat](class.evstat.html)
    
-   Повертає попередній набір значень, які повертаються EvStat::attr
    

# EvStat::prev

(PECL ev >= 0.2.0)

EvStat::prev — Повертає попередній набір значень, які повертаються EvStat::attr

### Опис

```methodsynopsis
public
   EvStat::prev(): void
```

Як і [EvStat::attr()](evstat.attr.html) але повертає попередній набір значень.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив з тією ж структурою, що і масив, що повертається [EvStat::attr()](evstat.attr.html). Масив містить попередній набір значень.

### Дивіться також

-   [EvStat::attr()](evstat.attr.html) - Повертає значення, нещодавно виявлені Ev
-   [EvStat::stat()](evstat.stat.html) - Ініціює виклик статистики