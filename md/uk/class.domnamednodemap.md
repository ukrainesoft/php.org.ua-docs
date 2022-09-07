---
navigation:
  - domimplementation.hasfeature.md: '« DOMImplementation::hasFeature'
  - domnamednodemap.count.md: 'DOMNamedNodeMap::count »'
  - index.md: PHP Manual
  - book.dom.md: DOM
title: Клас DOMNamedNodeMap
---
# Клас DOMNamedNodeMap

(PHP 5, PHP 7, PHP 8)

## Огляд класів

```classsynopsis

     
    

    
     
      class DOMNamedNodeMap
     

     implements 
       IteratorAggregate,  Countable {

    /* Свойства */
    
     public
     readonly
     int
      $length;


    /* Методы */
    
   public count(): int
public getNamedItem(string $qualifiedName): ?DOMNode
public getNamedItemNS(?string $namespace, string $localName): ?DOMNode
public item(int $index): ?DOMNode

   }
```

## Властивості

length

Кількість вузлів відображається. Діапазон допустимих індексів дочірніх вузлів `0` до `length - 1` включно.

## список змін

| Версия | Описание |
| --- | --- |
|  | Нереалізовані методи **DOMNamedNodeMap::setNamedItem()** **DOMNamedNodeMap::removeNamedItem()** **DOMNamedNodeMap::setNamedItemNS()** і **DOMNamedNodeMap::removeNamedItem()** були вилучені. |
|  | Клас **DOMNamedNodeMap** тепер реалізує інтерфейс [IteratorAggregate](class.iteratoraggregate.md). Раніше натомість було реалізовано інтерфейс [Traversable](class.traversable.md) |

## Зміст

-   [DOMNamedNodeMap::count](domnamednodemap.count.md) - Кількість вузлів у відображенні
-   [DOMNamedNodeMap::getNamedItem](domnamednodemap.getnameditem.md) — Отримує вузол, вказаний на ім'я
-   [DOMNamedNodeMap::getNamedItemNS](domnamednodemap.getnameditemns.md) — Отримує вузол із заданим локальним ім'ям та URI простору імен
-   [DOMNamedNodeMap::item](domnamednodemap.item.md) — Отримує вузол із заданим індексом
