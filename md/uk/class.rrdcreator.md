---
navigation:
  - function.rrdc-disconnect.md: « rrdc\_disconnect
  - rrdcreator.addarchive.md: 'RRDCreator::addArchive »'
  - index.md: PHP Manual
  - book.rrd.md: RRD
title: Клас RRDCreator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

-   [RRDCreator::addArchive](rrdcreator.addarchive.md)— Додає RRA – архів значень даних для кожного джерела даних
-   [RRDCreator::addDataSource](rrdcreator.adddatasource.md)— Додає визначення джерела даних для бази даних RRD
-   [RRDCreator::\_\_construct](rrdcreator.construct.md)— Створює новий екземпляр RRDCreator
-   [RRDCreator::save](rrdcreator.save.md)— Зберігає базу даних RRD у файл
