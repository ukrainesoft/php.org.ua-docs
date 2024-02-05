---
navigation:
  - domelement.prepend.md: '« DOMElement::prepend'
  - domelement.removeattribute.md: 'DOMElement::removeAttribute »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::remove'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMElement::remove

(PHP 8)

DOMElement::remove — Видаляє елемент

### Опис

```methodsynopsis
public DOMElement::remove(): void
```

Видаляє елемент.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад использования метода**DOMElement::remove()\*\*\*\*

Видалення елемента.

```php
<?php
$doc = new DOMDocument;
$doc->loadXML("<container><hello/><world/></container>");
$hello = $doc->documentElement->firstChild;

$hello->remove();

echo $doc->saveXML();
?>
```

Результат виконання наведеного прикладу:

```
<?xml version="1.0"?>
<container><world/></container>
```

### Дивіться також

-   [DOMElement::after()](domelement.after.md) \- Додає вузли після елемента
-   [DOMElement::before()](domelement.before.md) \- Додає вузли перед елементом
-   [DOMElement::replaceWith()](domelement.replacewith.md) \- Замінює елемент новими вузлами
-   [DOMNode::removeChild()](domnode.removechild.md) \- видаляє дочірній вузол зі списку нащадків
