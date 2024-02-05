---
navigation:
  - domnode.lookupnamespaceuri.md: '« DOMNode::lookupNamespaceURI'
  - domnode.normalize.md: 'DOMNode::normalize »'
  - index.md: PHP Manual
  - class.domnode.md: DOMNode
title: 'DOMNode::lookupPrefix'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Повертає префікс простору імен або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [DOMNode::lookupNamespaceUri()](domnode.lookupnamespaceuri.md) \- Отримує URI простору імен вузла за префіксом
