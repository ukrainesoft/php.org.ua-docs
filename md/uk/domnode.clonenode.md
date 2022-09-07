---
navigation:
  - domnode.c14nfile.md: '« DOMNode::C14NFile'
  - domnode.getlineno.md: 'DOMNode::getLineNo »'
  - index.md: PHP Manual
  - class.domnode.md: DOMNode
title: 'DOMNode::cloneNode'
---
# DOMNode::cloneNode

(PHP 5, PHP 7, PHP 8)

DOMNode::cloneNode — Клонує вузол

### Опис

```methodsynopsis
public DOMNode::cloneNode(bool $deep = false): DOMNode|false
```

Створює копію вузла.

### Список параметрів

`deep`

Вказує, чи потрібно копіювати нащадків. Цей параметр за замовчуванням має значення **`false`**

### Значення, що повертаються

Копія вузла.
