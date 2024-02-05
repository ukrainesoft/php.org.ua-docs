---
navigation:
  - domelement.setattributenode.md: '« DOMElement::setAttributeNode'
  - domelement.setattributens.md: 'DOMElement::setAttributeNS »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::setAttributeNodeNS'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMElement::setAttributeNodeNS

(PHP 5, PHP 7, PHP 8)

DOMElement::setAttributeNodeNS — Додає новий атрибут елемент

### Опис

```methodsynopsis
public DOMElement::setAttributeNodeNS(DOMAttr $attr): DOMAttr|null|false
```

Додає новий вузол атрибуту `attr` елемент з урахуванням простору імен. Якщо в елементі вже існує атрибут з таким самим ім'ям, то він замінюється на `attr`

### Список параметрів

`attr`

Вузол атрибуту.

### Значення, що повертаються

Повертає старий атрибут, якщо його замінили або **`null`**якщо старого атрибута не було. Якщо виникає помилка **`DOM_WRONG_DOCUMENT_ERR`**, а strictErrorChecking равно**`false`**, то повертається значення **`false`**

### Помилки

**`DOM_WRONG_DOCUMENT_ERR`**

Виникає, якщо параметр `attr` належить не даному елементу, а іншому документу.

### Дивіться також

-   [DOMElement::hasAttributeNS()](domelement.hasattributens.md) \- Перевіряє, чи існує заданий атрибут
-   [DOMElement::getAttributeNodeNS()](domelement.getattributenodens.md) \- Повертає вузол атрибуту
-   [DOMElement::removeAttributeNode()](domelement.removeattributenode.md) \- Видаляє атрибут
