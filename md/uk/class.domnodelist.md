Клас DOMNodeList

-   [« DOMNode::replaceChild](domnode.replacechild.html)
    
-   [DOMNodeList::count »](domnodelist.count.html)
    
-   [PHP Manual](index.html)
    
-   [DOM](book.dom.html)
    
-   Клас DOMNodeList
    

# Клас DOMNodeList

(PHP 5, PHP 7, PHP 8)

## Огляд класів

```classsynopsis

     
    

    
     
      class DOMNodeList
     

     implements 
       IteratorAggregate,  Countable {

    /* Свойства */
    
     public
     readonly
     int
      $length;


    /* Методы */
    
   public count(): int
public item(int $index): DOMNode|DOMNameSpaceNode|null

   }
```

## Властивості

length

Кількість вузлів у списку. Діапазон дійсних індексів дочірніх вузлів знаходиться у проміжку від 0 до `length - 1` включно.

## список змін

| Версия | Описание |
| --- | --- |
|  | Клас **DOMNodeList** тепер реалізує інтерфейс [IteratorAggregate](class.iteratoraggregate.html). Раніше натомість було реалізовано інтерфейс [Traversable](class.traversable.html) |
|  | Реалізовано інтерфейс [Countable](class.countable.html) та повертає значення властивості [length](class.domnodelist.html#domnodelist.props.length) |

## Дивіться також

-   [» Спецификация W3C по NodeList](http://www.w3.org/TR/2003/WD-DOM-Level-3-Core-20030226/DOM3-Core.html#core-ID-536297177)

## Зміст

-   [DOMNodeList::count](domnodelist.count.html) — Отримати кількість вузлів у списку
-   [DOMNodeList::item](domnodelist.item.html) — Отримує вузол із заданим індексом