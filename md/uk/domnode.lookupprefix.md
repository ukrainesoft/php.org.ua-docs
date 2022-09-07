---
navigation:
  - domnode.lookupnamespaceuri.md: '« DOMNode::lookupNamespaceUri'
  - domnode.normalize.md: 'DOMNode::normalize »'
  - index.md: PHP Manual
  - class.domnode.md: DOMNode
title: 'DOMNode::lookupPrefix'
---
# DOMNode::lookupPrefix

(PHP 5, PHP 7, PHP 8)

DOMNode::lookupPrefix — Повертає префікс простору імен вузла з URI простору імен

### Опис

```methodsynopsis
public DOMNode::lookupPrefix(string $namespace): ?string
```

Повертає префікс простору імен вузла з урахуванням URI простору імен.

### Список параметрів

`namespace`

URI простір імен.

### Значення, що повертаються

Префікс простору імен.

### Дивіться також

-   [DOMNode::lookupNamespaceUri()](domnode.lookupnamespaceuri.md) - Отримує URI простору імен вузла за префіксом
