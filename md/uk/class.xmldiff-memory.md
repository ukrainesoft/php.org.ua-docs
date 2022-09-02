---
navigation:
  - xmldiff-dom.merge.md: '« XMLDiffDOM::merge'
  - xmldiff-memory.diff.md: 'XMLDiffMemory::diff »'
  - index.md: PHP Manual
  - book.xmldiff.md: XMLDiff
title: Клас XMLDiffMemory
---
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

-   [XMLDiffMemory::diff](xmldiff-memory.diff.md) — Порівняння двох документів XML
-   [XMLDiffMemory::merge](xmldiff-memory.merge.md) — Застосувати зміни до документа XML
