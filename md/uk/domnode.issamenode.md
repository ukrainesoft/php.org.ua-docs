---
navigation:
  - domnode.isdefaultnamespace.html: '« DOMNode::isDefaultNamespace'
  - domnode.issupported.html: 'DOMNode::isSupported »'
  - index.html: PHP Manual
  - class.domnode.html: DOMNode
title: 'DOMNode::isSameNode'
---
# DOMNode::isSameNode

(PHP 5, PHP 7, PHP 8)

DOMNode::isSameNode — Вказує, чи є два вузли одним і тим же вузлом

### Опис

```methodsynopsis
public DOMNode::isSameNode(DOMNode $otherNode): bool
```

Ця функція вказує, чи є два вузли одним і тим самим вузлом. Це порівняння відбувається *не* на основі вмісту вузлів.

### Список параметрів

`otherNode`

Порівнюваний вузол.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
