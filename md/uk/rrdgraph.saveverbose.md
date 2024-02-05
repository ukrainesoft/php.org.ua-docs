---
navigation:
  - rrdgraph.save.md: '« RRDGraph::save'
  - rrdgraph.setoptions.md: 'RRDGraph::setOptions »'
  - index.md: PHP Manual
  - class.rrdgraph.md: RRDGraph
title: 'RRDGraph::saveVerbose'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RRDGraph::saveVerbose

(PECL rrd >= 0.9.0)

RRDGraph::saveVerbose — Зберігає запит до бази даних RRD у зображення та повертає докладну інформацію про згенерований графік

### Опис

```methodsynopsis
public RRDGraph::saveVerbose(): array
```

Зберігає запит до бази даних RRD у файл зображення, визначений методом [RRDGraph::\_\_construct()](rrdgraph.construct.md) і повертає докладну інформацію про згенерований графік, якщо як ім'я файлу зображення використовується "-", дані зображення також повертаються в масиві результатів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив з детальною інформацією про згенероване зображення, опціонально з даними зображення або \*\*`false`\*\*в случае возникновения ошибки.
