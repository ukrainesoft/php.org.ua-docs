Клас DOMImplementation

-   [« DOMException](class.domexception.html)
    
-   [DOMImplementation::\_\_construct »](domimplementation.construct.html)
    
-   [PHP Manual](index.html)
    
-   [DOM](book.dom.html)
    
-   Клас DOMImplementation
    

# Клас DOMImplementation

(PHP 5, PHP 7, PHP 8)

## Вступ

Клас **DOMImplementation** надає ряд методів для виконання операцій, які не залежать від будь-якого примірника об'єктної моделі документа.

## Огляд класів

```classsynopsis

     
    

    
     
      class DOMImplementation
     
     {

    /* Методы */
    
   public createDocument(?string $namespace = null, string $qualifiedName = "", ?DOMDocumentType $doctype = null): DOMDocument|false
public createDocumentType(string $qualifiedName, string $publicId = "", string $systemId = ""): DOMDocumentType|false
public hasFeature(string $feature, string $version): bool

   }
```

## Зміст

-   [DOMImplementation::\_\_construct](domimplementation.construct.html) — Створює новий об'єкт класу DOMImplementation
-   [DOMImplementation::createDocument](domimplementation.createdocument.html) — Створює об'єкт класу DOMDocument заданого типу з його елементом.
-   [DOMImplementation::createDocumentType](domimplementation.createdocumenttype.html) — Створює порожній об'єкт класу DOMDocumentType
-   [DOMImplementation::hasFeature](domimplementation.hasfeature.html) — Перевірка, чи реалізована певна можливість у реалізації DOM