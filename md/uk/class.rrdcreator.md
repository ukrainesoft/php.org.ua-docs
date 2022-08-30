Клас RRDCreator

-   [« rrdcdisconnect](function.rrdc-disconnect.html)
    
-   [RRDCreator::addArchive »](rrdcreator.addarchive.html)
    
-   [PHP Manual](index.html)
    
-   [RRD](book.rrd.html)
    
-   Клас RRDCreator
    

# Клас RRDCreator

(PECL rrd >= 0.9.0)

## Вступ

Клас створення файлів бази даних RRD.

## Огляд класів

```classsynopsis


    
    
     
      class RRDCreator
     
     {
    

    /* Методы */
    
   public __construct(string $path, string $startTime = ?, int $step = 0)

    public addArchive(string $description): void
public addDataSource(string $description): void
public save(): bool

   }
```

## Зміст

-   [RRDCreator::addArchive](rrdcreator.addarchive.html) — Додає RRA – архів значень даних для кожного джерела даних
-   [RRDCreator::addDataSource](rrdcreator.adddatasource.html) — Додає визначення джерела даних для бази даних RRD
-   [RRDCreator::construct](rrdcreator.construct.html) — Створює новий екземпляр RRDCreator
-   [RRDCreator::save](rrdcreator.save.html) — Зберігає базу даних RRD у файл