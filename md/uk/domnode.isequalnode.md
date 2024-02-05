---
navigation:
  - domnode.isdefaultnamespace.md: '« DOMNode::isDefaultNamespace'
  - domnode.issamenode.md: 'DOMNode::isSameNode »'
  - index.md: PHP Manual
  - class.domnode.md: DOMNode
title: 'DOMNode::isEqualNode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMNode::isEqualNode

(PHP 8 >= 8.3.0)

DOMNode::isEqualNode — Перевіряє, що обидва вузли ідентичні

### Опис

```methodsynopsis
public DOMNode::isEqualNode(?DOMNode $otherNode): bool
```

Перевіряє обидва вузли на ідентичність.

### Список параметрів

`otherNode`

Вузол.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо обидва вузли ідентичні, інакше **`false`**

### Приклади

**Приклад #1 Приклад использования метода**DOMNode::isEqualNode()\*\*\*\*

```php
<?php

$dom1 = (new DOMDocument())->createElement('h1', 'Привет, мир!');
$dom2 = (new DOMDocument())->createElement('h1', 'Привет, мир!');

var_dump($dom1->isEqualNode($dom2));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```
