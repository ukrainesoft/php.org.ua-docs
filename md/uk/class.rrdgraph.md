Клас RRDGraph

-   [« RRDCreator::save](rrdcreator.save.html)
    
-   [RRDGraph::construct »](rrdgraph.construct.html)
    
-   [PHP Manual](index.html)
    
-   [RRD](book.rrd.html)
    
-   Клас RRDGraph
    

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

-   [RRDGraph::construct](rrdgraph.construct.html) — Створює новий екземпляр RRDGraph
-   [RRDGraph::save](rrdgraph.save.html) — Зберігає результат запиту на зображення
-   [RRDGraph::saveVerbose](rrdgraph.saveverbose.html) — Зберігає запит до бази даних RRD у зображення та повертає докладну інформацію про згенерований графік
-   [RRDGraph::setOptions](rrdgraph.setoptions.html) — Встановлює параметри експорту графіка rrd