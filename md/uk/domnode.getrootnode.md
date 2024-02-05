---
navigation:
  - domnode.getnodepath.md: '« DOMNode::getNodePath'
  - domnode.hasattributes.md: 'DOMNode::hasAttributes »'
  - index.md: PHP Manual
  - class.domnode.md: DOMNode
title: 'DOMNode::getRootNode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMNode::getRootNode

(PHP 8 >= 8.3.0)

DOMNode::getRootNode — Отримує кореневий вузол

### Опис

```methodsynopsis
public DOMNode::getRootNode(array $options = null): DOMNode
```

Отримує кореневий вузол.

### Список параметрів

`options`

Параметр поки що ні на що не впливає.

### Значення, що повертаються

Повертає кореневий вузол.

### Приклади

**Пример #1 Пример использования метода**DOMNode::getRootNode()\*\*\*\*

```php
<?php

$dom = new DOMDocument();
$dom->loadXML('<?xml version="1.0"?><html><body/></html>');

var_dump($dom->documentElement->firstElementChild->getRootNode() === $dom);
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```
