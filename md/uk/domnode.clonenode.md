---
navigation:
  - domnode.c14nfile.md: '« DOMNode::C14NFile'
  - domnode.contains.md: 'DOMNode::contains »'
  - index.md: PHP Manual
  - class.domnode.md: DOMNode
title: 'DOMNode::cloneNode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Вказує, чи потрібно копіювати всіх нащадків. Цей параметр за замовчуванням має значення **`false`**

### Значення, що повертаються

Копія вузла.
