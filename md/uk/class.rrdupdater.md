---
navigation:
  - rrdgraph.setoptions.md: '« RRDGraph::setOptions'
  - rrdupdater.construct.md: 'RRDUpdater::\_\_construct »'
  - index.md: PHP Manual
  - book.rrd.md: RRD
title: Клас RRDUpdater
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

-   [RRDUpdater::\_\_construct](rrdupdater.construct.md)— Створює новий об'єкт RRDUpdater
-   [RRDUpdater::update](rrdupdater.update.md)— Оновлює файл бази даних RRD
