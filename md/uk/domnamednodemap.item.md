---
navigation:
  - domnamednodemap.getnameditemns.html: '« DOMNamedNodeMap::getNamedItemNS'
  - class.domnode.html: DOMNode »
  - index.html: PHP Manual
  - class.domnamednodemap.html: DOMNamedNodeMap
title: 'DOMNamedNodeMap::item'
---
# DOMNamedNodeMap::item

(PHP 5, PHP 7, PHP 8)

DOMNamedNodeMap::item — Отримує вузол із заданим індексом

### Опис

```methodsynopsis
public DOMNamedNodeMap::item(int $index): ?DOMNode
```

Витягує вузол із заданим індексом `index` з об'єкту класу [DOMNamedNodeMap](class.domnamednodemap.html)

### Список параметрів

`index`

Індекс вузла у відображенні.

### Значення, що повертаються

Вузол з індексом `index` у відображенні або \*\*`null`\*\*якщо індекс має неприпустиме значення (більше або дорівнює кількості вузлів у відображенні).
