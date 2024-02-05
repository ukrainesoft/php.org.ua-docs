---
navigation:
  - xmldiff.installation.md: « Встановлення
  - xmldiff-base.construct.md: 'XMLDiff\\Base::\_\_construct »'
  - index.md: PHP Manual
  - book.xmldiff.md: XMLDiff
title: Клас XMLDiff\\Base
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас XMLDiff\\Base

(PECL xmldiff >= 0.8.0)

## Вступ

Базовий абстрактний клас всім класів порівняння даного модуля.

## Огляд класів

```classsynopsis


    
    
     
      class XMLDiff\Base
     
     {
    

    /* Методы */
    
   public __construct(string $nsname)

    abstract public diff(mixed $from, mixed $to): mixed
abstract public merge(mixed $src, mixed $diff): mixed

   }
```

## Зміст

-   [XMLDiff\\Base::\_\_construct](xmldiff-base.construct.md) \- Конструктор
-   [XMLDiff\\Base::diff](xmldiff-base.diff.md)— Здійснює порівняння двох документів XML
-   [XMLDiff\\Base::merge](xmldiff-base.merge.md)— Створює новий документ XML, ґрунтуючись на інформації про його відмінність від іншого
