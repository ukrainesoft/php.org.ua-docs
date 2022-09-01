---
navigation:
  - domelement.removeattribute.html: '« DOMElement::removeAttribute'
  - domelement.removeattributens.html: 'DOMElement::removeAttributeNS »'
  - index.html: PHP Manual
  - class.domelement.html: DOMElement
title: 'DOMElement::removeAttributeNode'
---
# DOMElement::removeAttributeNode

(PHP 5, PHP 7, PHP 8)

DOMElement::removeAttributeNode — Видаляє атрибут

### Опис

```methodsynopsis
public DOMElement::removeAttributeNode(DOMAttr $attr): DOMAttr|false
```

Видаляє вузол атрибуту `attr` елемент.

### Список параметрів

`attr`

Вузол атрибуту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**

Виникає, якщо вузол доступний лише читання.

**`DOM_NOT_FOUND_ERROR`**

Виникає, якщо `attr` не є атрибутом елемента.

### Дивіться також

-   [DOMElement::hasAttribute()](domelement.hasattribute.html) - Перевіряє, чи існує атрибут
-   [DOMElement::getAttributeNode()](domelement.getattributenode.html) - Повертає вузол атрибуту
-   [DOMElement::setAttributeNode()](domelement.setattributenode.html) - Додає новий вузол атрибуту елемент
