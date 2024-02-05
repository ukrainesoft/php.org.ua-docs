---
navigation:
  - xmldiff-dom.merge.md: '« XMLDiff\\DOM::merge'
  - xmldiff-memory.diff.md: 'XMLDiff\\Memory::diff »'
  - index.md: PHP Manual
  - book.xmldiff.md: XMLDiff
title: Клас XMLDiff\\Memory
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас XMLDiff\\Memory

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

-   [XMLDiff\\Memory::diff](xmldiff-memory.diff.md)— Порівняння двох документів XML
-   [XMLDiff\\Memory::merge](xmldiff-memory.merge.md)— Застосувати зміни до документа XML
