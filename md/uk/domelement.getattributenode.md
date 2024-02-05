---
navigation:
  - domelement.getattributenames.md: '« DOMElement::getAttributeNames'
  - domelement.getattributenodens.md: 'DOMElement::getAttributeNodeNS »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::getAttributeNode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMElement::getAttributeNode

(PHP 5, PHP 7, PHP 8)

DOMElement::getAttributeNode — Повертає вузол атрибуту

### Опис

```methodsynopsis
public DOMElement::getAttributeNode(string $qualifiedName): DOMAttr|DOMNameSpaceNode|false
```

Повертає вузол атрибута з ім'ям `qualifiedName` поточного елемента.

### Список параметрів

`qualifiedName`

Ім'я атрибуту.

### Значення, що повертаються

Вузол атрибуту. Зверніть увагу, що для оголошень просторів імен XML (атрибути `xmlns`и`xmlns:*`) повертається екземпляр [DOMNameSpaceNode](class.domnamespacenode.md), а не[DOMAttr](class.domattr.md)

### Дивіться також

-   [DOMElement::hasAttribute()](domelement.hasattribute.md) \- Перевіряє, чи існує атрибут
-   [DOMElement::setAttributeNode()](domelement.setattributenode.md) \- Додає новий вузол атрибуту елемент
-   [DOMElement::removeAttributeNode()](domelement.removeattributenode.md) \- Видаляє атрибут
