Клас DOMNamedNodeMap

-   [« DOMImplementation::hasFeature](domimplementation.hasfeature.html)
    
-   [DOMNamedNodeMap::count »](domnamednodemap.count.html)
    
-   [PHP Manual](index.html)
    
-   [DOM](book.dom.html)
    
-   Клас DOMNamedNodeMap
    

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

| Версия | Описание                                                                                                                                                                                      |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Нереалізовані методи **DOMNamedNodeMap::setNamedItem()** **DOMNamedNodeMap::removeNamedItem()** **DOMNamedNodeMap::setNamedItemNS()** і **DOMNamedNodeMap::removeNamedItem()** були вилучені. |
|        | Клас **DOMNamedNodeMap** тепер реалізує інтерфейс [IteratorAggregate](class.iteratoraggregate.html). Раніше натомість було реалізовано інтерфейс [Traversable](class.traversable.html)        |

## Зміст

-   [DOMNamedNodeMap::count](domnamednodemap.count.html) - Кількість вузлів у відображенні
-   [DOMNamedNodeMap::getNamedItem](domnamednodemap.getnameditem.html) — Отримує вузол, вказаний на ім'я
-   [DOMNamedNodeMap::getNamedItemNS](domnamednodemap.getnameditemns.html) — Отримує вузол із заданим локальним ім'ям та URI простору імен
-   [DOMNamedNodeMap::item](domnamednodemap.item.html) — Отримує вузол із заданим індексом