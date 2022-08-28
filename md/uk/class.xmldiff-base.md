Клас XMLDiffBase

-   [« Установка](xmldiff.installation.html)
    
-   [XMLDiff\\Base::\_\_construct »](xmldiff-base.construct.html)
    
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

-   [XMLDiff\\Base::\_\_construct](xmldiff-base.construct.html) - Конструктор
-   [XMLDiff\\Base::diff](xmldiff-base.diff.html) — Здійснює порівняння двох документів XML
-   [XMLDiff\\Base::merge](xmldiff-base.merge.html) — Створює новий документ XML, ґрунтуючись на інформації про його відмінність від іншого