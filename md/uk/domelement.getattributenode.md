---
navigation:
  - domelement.getattribute.html: '« DOMElement::getAttribute'
  - domelement.getattributenodens.html: 'DOMElement::getAttributeNodeNS »'
  - index.html: PHP Manual
  - class.domelement.html: DOMElement
title: 'DOMElement::getAttributeNode'
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

Вузол атрибуту. Зверніть увагу, що для об'яв просторів імен XML (атрибути `xmlns` і `xmlns:*`) повертається екземпляр **DOMNameSpaceNode**, а не [DOMAttr](class.domattr.html)

### Дивіться також

-   [DOMElement::hasAttribute()](domelement.hasattribute.html) - Перевіряє, чи існує атрибут
-   [DOMElement::setAttributeNode()](domelement.setattributenode.html) - Додає новий вузол атрибуту елемент
-   [DOMElement::removeAttributeNode()](domelement.removeattributenode.html) - Видаляє атрибут
