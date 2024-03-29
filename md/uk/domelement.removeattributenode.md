---
navigation:
  - domelement.removeattribute.md: '« DOMElement::removeAttribute'
  - domelement.removeattributens.md: 'DOMElement::removeAttributeNS »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::removeAttributeNode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMElement::removeAttributeNode

(PHP 5, PHP 7, PHP 8)

DOMElement::removeAttributeNode — Видаляє атрибут

### Опис

```methodsynopsis
public DOMElement::removeAttributeNode(DOMAttr $attr): DOMAttr|false
```

Удаляет узел атрибута`attr` елемент.

### Список параметрів

`attr`

Вузол атрибуту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**

Виникає, якщо вузол доступний лише читання.

**`DOM_NOT_FOUND_ERROR`**

Виникає, якщо `attr` не є атрибутом елемента.

### Дивіться також

-   [DOMElement::hasAttribute()](domelement.hasattribute.md) \- Перевіряє, чи існує атрибут
-   [DOMElement::getAttributeNode()](domelement.getattributenode.md) \- Повертає вузол атрибуту
-   [DOMElement::setAttributeNode()](domelement.setattributenode.md) \- Додає новий вузол атрибуту елемент
