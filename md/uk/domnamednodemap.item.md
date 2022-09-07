---
navigation:
  - domnamednodemap.getnameditemns.md: '« DOMNamedNodeMap::getNamedItemNS'
  - class.domnode.md: DOMNode »
  - index.md: PHP Manual
  - class.domnamednodemap.md: DOMNamedNodeMap
title: 'DOMNamedNodeMap::item'
---
# DOMNamedNodeMap::item

(PHP 5, PHP 7, PHP 8)

DOMNamedNodeMap::item — Отримує вузол із заданим індексом

### Опис

```methodsynopsis
public DOMNamedNodeMap::item(int $index): ?DOMNode
```

Витягує вузол із заданим індексом `index` з об'єкту класу [DOMNamedNodeMap](class.domnamednodemap.md)

### Список параметрів

`index`

Індекс вузла у відображенні.

### Значення, що повертаються

Вузол з індексом `index` у відображенні або \*\*`null`\*\*якщо індекс має неприпустиме значення (більше або дорівнює кількості вузлів у відображенні).
