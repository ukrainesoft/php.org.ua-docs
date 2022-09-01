---
navigation:
  - domelement.removeattributens.html: '« DOMElement::removeAttributeNS'
  - domelement.setattributenode.html: 'DOMElement::setAttributeNode »'
  - index.html: PHP Manual
  - class.domelement.html: DOMElement
title: 'DOMElement::setAttribute'
---
# DOMElement::setAttribute

(PHP 5, PHP 7, PHP 8)

DOMElement::setAttribute — Додає новий або змінює існуючий атрибут

### Опис

```methodsynopsis
public DOMElement::setAttribute(string $qualifiedName, string $value): DOMAttr|bool
```

Встановлює атрибут з ім'ям `qualifiedName`. Якщо атрибут не існує, він буде створений.

### Список параметрів

`qualifiedName`

Ім'я атрибуту.

`value`

Значення атрибуту.

### Значення, що повертаються

Створений чи змінений об'єкт класу [DOMAttr](class.domattr.html) або **`false`** у разі виникнення помилки.

### Помилки

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**

Виникає, якщо вузол доступний лише читання.

### Приклади

**Приклад #1 Встановлення значення атрибута**

```php
<?php
$doc = new DOMDocument("1.0");
$node = $doc->createElement("para");
$newnode = $doc->appendChild($node);
$newnode->setAttribute("align", "left");
?>
```

### Дивіться також

-   [DOMElement::hasAttribute()](domelement.hasattribute.html) - Перевіряє, чи існує атрибут
-   [DOMElement::getAttribute()](domelement.getattribute.html) - Повертає значення атрибуту
-   [DOMElement::removeAttribute()](domelement.removeattribute.html) - Видаляє атрибут
