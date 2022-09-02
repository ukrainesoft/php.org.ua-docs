---
navigation:
  - rrdcreator.save.md: '« RRDCreator::save'
  - rrdgraph.construct.md: 'RRDGraph::construct »'
  - index.md: PHP Manual
  - book.rrd.md: RRD
title: Клас RRDGraph
---
# Клас RRDGraph

(PECL rrd >= 0.9.0)

## Вступ

Клас для експорту даних із файлу бази даних RRD у зображення.

## Огляд класів

```classsynopsis


    
    
     
      class RRDGraph
     
     {
    

    /* Методы */
    
   public __construct(string $path)

    public save(): array
public saveVerbose(): array
public setOptions(array $options): void

   }
```

## Зміст

-   [RRDGraph::construct](rrdgraph.construct.md) — Створює новий екземпляр RRDGraph
-   [RRDGraph::save](rrdgraph.save.md) — Зберігає результат запиту на зображення
-   [RRDGraph::saveVerbose](rrdgraph.saveverbose.md) — Зберігає запит до бази даних RRD у зображення та повертає докладну інформацію про згенерований графік
-   [RRDGraph::setOptions](rrdgraph.setoptions.md) — Встановлює параметри експорту графіка rrd
