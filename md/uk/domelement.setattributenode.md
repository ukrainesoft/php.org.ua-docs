---
navigation:
  - domelement.setattribute.md: '« DOMElement::setAttribute'
  - domelement.setattributenodens.md: 'DOMElement::setAttributeNodeNS »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::setAttributeNode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMElement::setAttributeNode

(PHP 5, PHP 7, PHP 8)

DOMElement::setAttributeNode — Додає новий вузол атрибута до елементу

### Опис

```methodsynopsis
public DOMElement::setAttributeNode(DOMAttr $attr): DOMAttr|null|false
```

Додає новий вузол атрибуту `attr` елемент. Якщо в елементі вже існує вузол з таким самим ім'ям, то він замінюється на `attr`

### Список параметрів

`attr`

Вузол атрибуту.

### Значення, що повертаються

Повертає старий вузол, якщо він був замінений або **`null`**якщо старого вузла не було. Якщо видається помилка **`DOM_WRONG_DOCUMENT_ERR`**, а strictErrorChecking равно**`false`**, то повертається **`false`**

### Помилки

**`DOM_WRONG_DOCUMENT_ERR`**

Виникає, якщо параметр `attr`принадлежит не данному узлу, а другому документу.

### Дивіться також

-   [DOMElement::hasAttribute()](domelement.hasattribute.md) \- Перевіряє, чи існує атрибут
-   [DOMElement::getAttributeNode()](domelement.getattributenode.md) \- Повертає вузол атрибуту
-   [DOMElement::removeAttributeNode()](domelement.removeattributenode.md) \- Видаляє атрибут
