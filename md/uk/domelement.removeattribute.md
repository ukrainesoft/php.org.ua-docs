---
navigation:
  - domelement.hasattributens.md: '« DOMElement::hasAttributeNS'
  - domelement.removeattributenode.md: 'DOMElement::removeAttributeNode »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::removeAttribute'
---
# DOMElement::removeAttribute

(PHP 5, PHP 7, PHP 8)

DOMElement::removeAttribute — Видаляє атрибут

### Опис

```methodsynopsis
public DOMElement::removeAttribute(string $qualifiedName): bool
```

Видаляє атрибут з ім'ям `qualifiedName` елемент.

### Список параметрів

`qualifiedName`

Ім'я атрибуту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**

Виникає, якщо атрибут доступний лише для читання.

### Дивіться також

-   [DOMElement::hasAttribute()](domelement.hasattribute.md) - Перевіряє, чи існує атрибут
-   [DOMElement::getAttribute()](domelement.getattribute.md) - Повертає значення атрибуту
-   [DOMElement::setAttribute()](domelement.setattribute.md) - Додає новий або змінює існуючий атрибут
