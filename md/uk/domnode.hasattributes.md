---
navigation:
  - domnode.getrootnode.md: '« DOMNode::getRootNode'
  - domnode.haschildnodes.md: 'DOMNode::hasChildNodes »'
  - index.md: PHP Manual
  - class.domnode.md: DOMNode
title: 'DOMNode::hasAttributes'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMNode::hasAttributes

(PHP 5, PHP 7, PHP 8)

DOMNode::hasAttributes — Перевіряє, чи цей вузол має атрибути.

### Опис

```methodsynopsis
public DOMNode::hasAttributes(): bool
```

Цей метод перевіряє, чи поточний вузол містить атрибути. Вузол, що перевіряється, повинен бути **`XML_ELEMENT_NODE`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [DOMNode::hasChildNodes()](domnode.haschildnodes.md) \- Перевіряє, чи має цей вузол нащадків
