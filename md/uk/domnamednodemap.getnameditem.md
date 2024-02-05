---
navigation:
  - domnamednodemap.getiterator.md: '« DOMNamedNodeMap::getIterator'
  - domnamednodemap.getnameditemns.md: 'DOMNamedNodeMap::getNamedItemNS »'
  - index.md: PHP Manual
  - class.domnamednodemap.md: DOMNamedNodeMap
title: 'DOMNamedNodeMap::getNamedItem'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMNamedNodeMap::getNamedItem

(PHP 5, PHP 7, PHP 8)

DOMNamedNodeMap::getNamedItem — Отримує вузол, вказаний на ім'я

### Опис

```methodsynopsis
public DOMNamedNodeMap::getNamedItem(string $qualifiedName): ?DOMNode
```

Извлекает узел по заданному`nodeName`

### Список параметрів

`qualifiedName`

Имя`nodeName` шуканого вузла.

### Значення, що повертаються

Вузол (будь-якого типу) із заданим значенням тега `nodeName`или\*\*`null`\*\*якщо таких не знайдено.

### Дивіться також

-   [DOMNamedNodeMap::getNamedItemNS()](domnamednodemap.getnameditemns.md) \- Отримує вузол із заданим локальним ім'ям та URI простору імен
