---
navigation:
  - rrdgraph.setoptions.html: '« RRDGraph::setOptions'
  - rrdupdater.construct.html: 'RRDUpdater::construct »'
  - index.html: PHP Manual
  - book.rrd.html: RRD
title: Клас RRDUpdater
---
# Клас RRDUpdater

(PECL rrd >= 0.9.0)

## Вступ

Клас оновлення файлу бази даних RDD.

## Огляд класів

```classsynopsis


    
    
     
      class RRDUpdater
     
     {
    

    /* Методы */
    
   public __construct(string $path)

    public update(array $values, string $time
     = time()
   ): bool

   }
```

## Зміст

-   [RRDUpdater::construct](rrdupdater.construct.html) — Створює новий об'єкт RRDUpdater
-   [RRDUpdater::update](rrdupdater.update.html) — Оновлює файл бази даних RRD
