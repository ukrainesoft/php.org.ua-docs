---
navigation:
  - domnode.getnodepath.md: '« DOMNode::getNodePath'
  - domnode.haschildnodes.md: 'DOMNode::hasChildNodes »'
  - index.md: PHP Manual
  - class.domnode.md: DOMNode
title: 'DOMNode::hasAttributes'
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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [DOMNode::hasChildNodes()](domnode.haschildnodes.md) - Перевіряє, чи має цей вузол нащадків
