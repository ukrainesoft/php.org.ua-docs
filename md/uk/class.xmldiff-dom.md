Клас XMLDiffDOM

-   [« XMLDiffBase::merge](xmldiff-base.merge.html)
    
-   [XMLDiffDOM::diff »](xmldiff-dom.diff.html)
    
-   [PHP Manual](index.html)
    
-   [XMLDiff](book.xmldiff.html)
    
-   Клас XMLDiffDOM
    

# Клас XMLDiffDOM

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

-   [XMLDiffDOM::diff](xmldiff-dom.diff.html) — Пошук відмінностей у двох об'єктах DOMDocument
-   [XMLDiffDOM::merge](xmldiff-dom.merge.html) — Об'єднує об'єкт DOMDocument на основі іншого об'єкта DOMDocument, отриманого за допомогою XMLDiffDOM::diff