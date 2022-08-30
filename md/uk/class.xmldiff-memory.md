Клас XMLDiffMemory

-   [« XMLDiffDOM::merge](xmldiff-dom.merge.html)
    
-   [XMLDiffMemory::diff »](xmldiff-memory.diff.html)
    
-   [PHP Manual](index.html)
    
-   [XMLDiff](book.xmldiff.html)
    
-   Клас XMLDiffMemory
    

# Клас XMLDiffMemory

(PECL xmldiff >= 0.8.0)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class XMLDiff\Memory
     

     
      extends
       XMLDiff\Base
     
     {
    

    /* Методы */
    
   public diff(string $from, string $to): string
public merge(string $src, string $diff): string


    /* Наследуемые методы */
    abstract public XMLDiff\Base::diff(mixed $from, mixed $to): mixed
abstract public XMLDiff\Base::merge(mixed $src, mixed $diff): mixed


   }
```

## Зміст

-   [XMLDiffMemory::diff](xmldiff-memory.diff.html) — Порівняння двох документів XML
-   [XMLDiffMemory::merge](xmldiff-memory.merge.html) — Застосувати зміни до документа XML