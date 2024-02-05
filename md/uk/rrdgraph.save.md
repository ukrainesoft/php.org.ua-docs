---
navigation:
  - rrdgraph.construct.md: '« RRDGraph::\_\_construct'
  - rrdgraph.saveverbose.md: 'RRDGraph::saveVerbose »'
  - index.md: PHP Manual
  - class.rrdgraph.md: RRDGraph
title: 'RRDGraph::save'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RRDGraph::save

(PECL rrd >= 0.9.0)

RRDGraph::save — Зберігає результат запиту на зображення

### Опис

```methodsynopsis
public RRDGraph::save(): array
```

Зберігає результат запиту до бази даних RRD у зображення, визначене методом [RRDGraph::\_\_construct()](rrdgraph.construct.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертається масив з інформацією про згенероване зображення або \*\*`false`\*\*в случае возникновения ошибки.
