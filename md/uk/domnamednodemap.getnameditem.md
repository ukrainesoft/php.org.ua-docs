Отримує вузол, вказаний на ім'я

-   [« DOMNamedNodeMap::count](domnamednodemap.count.html)
    
-   [DOMNamedNodeMap::getNamedItemNS »](domnamednodemap.getnameditemns.html)
    
-   [PHP Manual](index.html)
    
-   [DOMNamedNodeMap](class.domnamednodemap.html)
    
-   Отримує вузол, вказаний на ім'я
    

# DOMNamedNodeMap::getNamedItem

(PHP 5, PHP 7, PHP 8)

DOMNamedNodeMap::getNamedItem — Отримує вузол, вказаний на ім'я

### Опис

```methodsynopsis
public DOMNamedNodeMap::getNamedItem(string $qualifiedName): ?DOMNode
```

Витягує вузол по заданому `nodeName`

### Список параметрів

`qualifiedName`

Ім'я `nodeName` шуканого вузла.

### Значення, що повертаються

Вузол (будь-якого типу) із заданим значенням тега `nodeName` або \*\*`null`\*\*якщо таких не знайдено.

### Дивіться також

-   [DOMNamedNodeMap::getNamedItemNS()](domnamednodemap.getnameditemns.html) - Отримує вузол із заданим локальним ім'ям та URI простору імен