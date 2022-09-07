---
navigation:
  - class.domchildnode.md: « DOMChildNode
  - domchildnode.before.md: 'DOMChildNode::before »'
  - index.md: PHP Manual
  - class.domchildnode.md: DOMChildNode
title: 'DOMChildNode::after'
---
# DOMChildNode::after

(PHP 8)

DOMChildNode::after — Додає вузли після вузла

### Опис

```methodsynopsis
public DOMChildNode::after(DOMNode|string ...$nodes): void
```

Додає передані `nodes` після вузла.

### Список параметрів

`nodes`

Вузли, які потрібно додати після вузла.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [DOMChildNode::before()](domchildnode.before.md) - Додає вузли перед вузлом
-   [DOMChildNode::remove()](domchildnode.remove.md) - видаляє вузол
-   [DOMChildNode::replaceWith()](domchildnode.replacewith.md) - Замінює вузол новими вузлами
-   [DOMNode::appendChild()](domnode.appendchild.md) - Додає новий дочірній вузол до кінця списку нащадків
