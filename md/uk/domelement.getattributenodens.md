---
navigation:
  - domelement.getattributenode.md: '« DOMElement::getAttributeNode'
  - domelement.getattributens.md: 'DOMElement::getAttributeNS »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::getAttributeNodeNS'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMElement::getAttributeNodeNS

(PHP 5, PHP 7, PHP 8)

DOMElement::getAttributeNodeNS — Повертає вузол атрибуту

### Опис

```methodsynopsis
public DOMElement::getAttributeNodeNS(?string $namespace, string $localName): DOMAttr|DOMNameSpaceNode|null
```

Повертає вузол атрибута у просторі імен `namespace` з локальним ім'ям `localName` для поточного сайту.

### Список параметрів

`namespace`

URI простір імен.

`localName`

Місцеве ім'я.

### Значення, що повертаються

Вузол атрибуту. Зверніть увагу, що для оголошень просторів імен XML (атрибути `xmlns`и`xmlns:*`) повертається екземпляр [DOMNameSpaceNode](class.domnamespacenode.md), а не об'єкт [DOMAttr](class.domattr.md)

### Дивіться також

-   [DOMElement::hasAttributeNS()](domelement.hasattributens.md) \- Перевіряє, чи існує заданий атрибут
-   [DOMElement::setAttributeNodeNS()](domelement.setattributenodens.md) \- Додає новий атрибут елемент
-   [DOMElement::removeAttributeNode()](domelement.removeattributenode.md) \- Видаляє атрибут
