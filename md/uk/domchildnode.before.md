---
navigation:
  - domchildnode.after.md: '« DOMChildNode::after'
  - domchildnode.remove.md: 'DOMChildNode::remove »'
  - index.md: PHP Manual
  - class.domchildnode.md: DOMChildNode
title: 'DOMChildNode::before'
---
# DOMChildNode::before

(PHP 8)

DOMChildNode::before — Додає вузли перед вузлом.

### Опис

```methodsynopsis
public DOMChildNode::before(DOMNode|string ...$nodes): void
```

Додає передані `nodes` перед вузлом.

### Список параметрів

`nodes`

Вузли, які потрібно додати перед вузлом.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [DOMChildNode::after()](domchildnode.after.md) - Додає вузли після вузла
-   [DOMChildNode::remove()](domchildnode.remove.md) - видаляє вузол
-   [DOMChildNode::replaceWith()](domchildnode.replacewith.md) - Замінює вузол новими вузлами
