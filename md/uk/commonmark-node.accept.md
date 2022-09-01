---
navigation:
  - commonmark-node.unlink.html: '« CommonMarkNode::unlink'
  - class.commonmark-interfaces-ivisitor.html: CommonMarkInterfacesIVisitor »
  - index.md: PHP Manual
  - class.commonmark-node.html: CommonMarkNode
title: 'CommonMarkNode::accept'
---
# CommonMarkNode::accept

(cmark >= 1.0.0)

CommonMarkNode::accept — Visitation

### Опис

```methodsynopsis
public CommonMark\Node::accept(CommonMark\Interfaces\IVisitor $visitor): void
```

### Список параметрів

`visitor`

Об'єкт, що реалізує [CommonMarkInterfacesIVisitor](class.commonmark-interfaces-ivisitor.html)

### Дивіться також

-   [CommonMarkInterfacesIVisitor::enter](commonmark-interfaces-ivisitor.enter.html)
-   [CommonMarkInterfacesIVisitor::leave](commonmark-interfaces-ivisitor.leave.html)
