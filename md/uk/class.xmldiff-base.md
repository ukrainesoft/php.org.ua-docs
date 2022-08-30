Клас XMLDiffBase

-   [« Установка](xmldiff.installation.html)
    
-   [XMLDiffBase::construct »](xmldiff-base.construct.html)
    
-   [PHP Manual](index.html)
    
-   [XMLDiff](book.xmldiff.html)
    
-   Клас XMLDiffBase
    

# Клас XMLDiffBase

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

-   [XMLDiffBase::construct](xmldiff-base.construct.html) - Конструктор
-   [XMLDiffBase::diff](xmldiff-base.diff.html) — Здійснює порівняння двох документів XML
-   [XMLDiffBase::merge](xmldiff-base.merge.html) — Створює новий документ XML, ґрунтуючись на інформації про його відмінність від іншого