---
navigation:
  - domnode.replacechild.md: '« DOMNode::replaceChild'
  - domnodelist.count.md: 'DOMNodeList::count »'
  - index.md: PHP Manual
  - book.dom.md: DOM
title: Клас DOMNodeList
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас DOMNodeList

(PHP 5, PHP 7, PHP 8)

## Огляд класів

```classsynopsis

    
     class DOMNodeList
    

    
     implements
      IteratorAggregate,

     Countable {

    /* Свойства */
    
     public
     readonly
     int
      $length;


    /* Методы */
    
   public count(): int
public getIterator(): Iterator
public item(int $index): DOMElement|DOMNode|DOMNameSpaceNode|null

   }
```

## Властивості

length

Кількість вузлів у списку. Діапазон дійсних індексів дочірніх вузлів знаходиться у проміжку від 0 до `length — 1` включно.

## список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Класс**DOMNodeList** тепер реалізує інтерфейс [IteratorAggregate](class.iteratoraggregate.md). . Раніше натомість було реалізовано інтерфейс [Traversable](class.traversable.md) |
| 7.2.0 | Реалізовано інтерфейс [Countable](class.countable.md) та повертає значення властивості [length](class.domnodelist.md#domnodelist.props.length) |

## Дивіться також

-   [» Специфікація W3C за NodeList](http://www.w3.org/TR/2003/WD-DOM-Level-3-Core-20030226/DOM3-Core.md#core-ID-536297177)

## Зміст

-   [DOMNodeList::count](domnodelist.count.md)— Отримати кількість вузлів у списку
-   [DOMNodeList::getIterator](domnodelist.getiterator.md)— Отримує зовнішній ітератор
-   [DOMNodeList::item](domnodelist.item.md)— Отримує вузол із заданим індексом
