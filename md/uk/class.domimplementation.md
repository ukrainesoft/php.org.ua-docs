---
navigation:
  - class.domexception.md: « DOMException
  - domimplementation.construct.md: 'DOMImplementation::\_\_construct »'
  - index.md: PHP Manual
  - book.dom.md: DOM
title: Клас DOMImplementation
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас DOMImplementation

(PHP 5, PHP 7, PHP 8)

## Вступ

Класс**DOMImplementation** надає низку методів для виконання операцій, які не залежать від будь-якого екземпляра об'єктної моделі документа.

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

-   [DOMImplementation::\_\_construct](domimplementation.construct.md)— Створює новий об'єкт класу DOMImplementation
-   [DOMImplementation::createDocument](domimplementation.createdocument.md)— Створює об'єкт класу DOMDocument заданого типу з його елементом.
-   [DOMImplementation::createDocumentType](domimplementation.createdocumenttype.md)— Створює порожній об'єкт класу DOMDocumentType
-   [DOMImplementation::hasFeature](domimplementation.hasfeature.md)— Перевірка, чи реалізована певна можливість у реалізації DOM
