---
navigation:
  - domelement.setattribute.md: '« DOMElement::setAttribute'
  - domelement.setattributenodens.md: 'DOMElement::setAttributeNodeNS »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::setAttributeNode'
---
# DOMElement::setAttributeNode

(PHP 5, PHP 7, PHP 8)

DOMElement::setAttributeNode — Додає новий вузол атрибута до елементу

### Опис

```methodsynopsis
public DOMElement::setAttributeNode(DOMAttr $attr): DOMAttr|null|false
```

Додає новий вузол атрибуту `attr` елемент.

### Список параметрів

`attr`

Вузол атрибуту.

### Значення, що повертаються

Повертає старий вузол, якщо атрибут замінено або **`null`**

### Помилки

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**

Виникає, якщо вузол доступний лише читання.

### Дивіться також

-   [DOMElement::hasAttribute()](domelement.hasattribute.md) - Перевіряє, чи існує атрибут
-   [DOMElement::getAttributeNode()](domelement.getattributenode.md) - Повертає вузол атрибуту
-   [DOMElement::removeAttributeNode()](domelement.removeattributenode.md) - Видаляє атрибут
