---
navigation:
  - domnode.isequalnode.md: '« DOMNode::isEqualNode'
  - domnode.issupported.md: 'DOMNode::isSupported »'
  - index.md: PHP Manual
  - class.domnode.md: DOMNode
title: 'DOMNode::isSameNode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMNode::isSameNode

(PHP 5, PHP 7, PHP 8)

DOMNode::isSameNode — Вказує, чи є два вузли одним і тим же вузлом

### Опис

```methodsynopsis
public DOMNode::isSameNode(DOMNode $otherNode): bool
```

Ця функція вказує, чи є два вузли тим самим вузлом. Це порівняння відбувається *не* на основі вмісту вузлів.

### Список параметрів

`otherNode`

Порівнюваний вузол.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
