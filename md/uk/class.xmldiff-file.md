Клас XMLDiffFile

-   [« XMLDiff\\Memory::merge](xmldiff-memory.merge.html)
    
-   [XMLDiff\\File::diff »](xmldiff-file.diff.html)
    
-   [PHP Manual](index.html)
    
-   [XMLDiff](book.xmldiff.html)
    
-   Клас XMLDiffFile
    

# Клас XMLDiffFile

(PECL xmldiff >= 0.8.0)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class XMLDiff\File
     

     
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

-   [XMLDiff\\File::diff](xmldiff-file.diff.html) — Порівняння двох файлів XML
-   [XMLDiff\\File::merge](xmldiff-file.merge.html) — Застосувати зміни до документа XML