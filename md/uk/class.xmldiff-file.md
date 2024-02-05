---
navigation:
  - xmldiff-memory.merge.md: '« XMLDiff\\Memory::merge'
  - xmldiff-file.diff.md: 'XMLDiff\\File::diff »'
  - index.md: PHP Manual
  - book.xmldiff.md: XMLDiff
title: Клас XMLDiff\\File
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас XMLDiff\\File

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

-   [XMLDiff\\File::diff](xmldiff-file.diff.md)— Порівняння двох файлів XML
-   [XMLDiff\\File::merge](xmldiff-file.merge.md)— Застосувати зміни до документа XML
