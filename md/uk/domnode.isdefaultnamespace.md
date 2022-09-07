---
navigation:
  - domnode.insertbefore.md: '« DOMNode::insertBefore'
  - domnode.issamenode.md: 'DOMNode::isSameNode »'
  - index.md: PHP Manual
  - class.domnode.md: DOMNode
title: 'DOMNode::isDefaultNamespace'
---
# DOMNode::isDefaultNamespace

(PHP 5, PHP 7, PHP 8)

DOMNode::isDefaultNamespace — Перевіряє, чи є вказаний URI простору імен вузла простором імен за промовчанням чи ні

### Опис

```methodsynopsis
public DOMNode::isDefaultNamespace(string $namespace): bool
```

Вказує, чи є `namespace` простір імен за замовчуванням.

### Список параметрів

`namespace`

URI простір імен.

### Значення, що повертаються

Повертає **`true`**, якщо `namespace` є простором імен за замовчуванням, **`false`** в іншому випадку.
