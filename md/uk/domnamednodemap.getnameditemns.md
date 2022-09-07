---
navigation:
  - domnamednodemap.getnameditem.md: '« DOMNamedNodeMap::getNamedItem'
  - domnamednodemap.item.md: 'DOMNamedNodeMap::item »'
  - index.md: PHP Manual
  - class.domnamednodemap.md: DOMNamedNodeMap
title: 'DOMNamedNodeMap::getNamedItemNS'
---
# DOMNamedNodeMap::getNamedItemNS

(PHP 5, PHP 7, PHP 8)

DOMNamedNodeMap::getNamedItemNS — Отримує вузол із заданим локальним ім'ям та URI простору імен

### Опис

```methodsynopsis
public DOMNamedNodeMap::getNamedItemNS(?string $namespace, string $localName): ?DOMNode
```

Витягує вузол із заданим локальним ім'ям `localName` та URI простору імен `namespace`

### Список параметрів

`namespace`

URI простору імен шуканого вузла.

`localName`

Локальне ім'я вузла, що шукається.

### Значення, що повертаються

Вузол (будь-якого типу) із заданим локальним ім'ям і URI простору імен або \*\*`null`\*\*якщо він не знайдений.

### Дивіться також

-   [DOMNamedNodeMap::getNamedItem()](domnamednodemap.getnameditem.md) - Отримує вузол, вказаний на ім'я
