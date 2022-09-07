---
navigation:
  - xmldiff-memory.merge.md: '« XMLDiffMemory::merge'
  - xmldiff-file.diff.md: 'XMLDiffFile::diff »'
  - index.md: PHP Manual
  - book.xmldiff.md: XMLDiff
title: Клас XMLDiffFile
---
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

-   [XMLDiffFile::diff](xmldiff-file.diff.md) — Порівняння двох файлів XML
-   [XMLDiffFile::merge](xmldiff-file.merge.md) — Застосувати зміни до документа XML
