---
navigation:
  - class.domexception.md: « DOMException
  - domimplementation.construct.md: 'DOMImplementation::construct »'
  - index.md: PHP Manual
  - book.dom.md: DOM
title: Клас DOMImplementation
---
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

-   [DOMImplementation::construct](domimplementation.construct.md) — Створює новий об'єкт класу DOMImplementation
-   [DOMImplementation::createDocument](domimplementation.createdocument.md) — Створює об'єкт класу DOMDocument заданого типу з його елементом.
-   [DOMImplementation::createDocumentType](domimplementation.createdocumenttype.md) — Створює порожній об'єкт класу DOMDocumentType
-   [DOMImplementation::hasFeature](domimplementation.hasfeature.md) — Перевірка, чи реалізована певна можливість у реалізації DOM
