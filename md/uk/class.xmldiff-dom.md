---
navigation:
  - xmldiff-base.merge.md: '« XMLDiff\\Base::merge'
  - xmldiff-dom.diff.md: 'XMLDiff\\DOM::diff »'
  - index.md: PHP Manual
  - book.xmldiff.md: XMLDiff
title: Клас XMLDiff\\DOM
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас XMLDiff\\DOM

(PECL xmldiff >= 0.8.0)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class XMLDiff\DOM
     

     
      extends
       XMLDiff\Base
     
     {
    

    /* Методы */
    
   public diff(DOMDocument $from, DOMDocument $to): DOMDocument
public merge(DOMDocument $src, DOMDocument $diff): DOMDocument


    /* Наследуемые методы */
    abstract public XMLDiff\Base::diff(mixed $from, mixed $to): mixed
abstract public XMLDiff\Base::merge(mixed $src, mixed $diff): mixed


   }
```

## Зміст

-   [XMLDiff\\DOM::diff](xmldiff-dom.diff.md)— Пошук відмінностей у двох об'єктах DOMDocument
-   [XMLDiff\\DOM::merge](xmldiff-dom.merge.md)— Об'єднує об'єкт DOMDocument на основі іншого об'єкта DOMDocument, отриманого за допомогою XMLDiff\\DOM::diff
