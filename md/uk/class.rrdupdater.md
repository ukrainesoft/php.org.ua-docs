Клас RRDUpdater

-   [« RRDGraph::setOptions](rrdgraph.setoptions.html)
    
-   [RRDUpdater::construct »](rrdupdater.construct.html)
    
-   [PHP Manual](index.html)
    
-   [RRD](book.rrd.html)
    
-   Клас RRDUpdater
    

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