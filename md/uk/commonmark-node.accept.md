---
navigation:
  - commonmark-node.unlink.md: '« CommonMarkNode::unlink'
  - class.commonmark-interfaces-ivisitor.md: CommonMarkInterfacesIVisitor »
  - index.md: PHP Manual
  - class.commonmark-node.md: CommonMarkNode
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

Об'єкт, що реалізує [CommonMarkInterfacesIVisitor](class.commonmark-interfaces-ivisitor.md)

### Дивіться також

-   [CommonMarkInterfacesIVisitor::enter](commonmark-interfaces-ivisitor.enter.md)
-   [CommonMarkInterfacesIVisitor::leave](commonmark-interfaces-ivisitor.leave.md)
