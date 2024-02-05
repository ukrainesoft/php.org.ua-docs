---
navigation:
  - domelement.replacewith.md: '« DOMElement::replaceWith'
  - domelement.setattributenode.md: 'DOMElement::setAttributeNode »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::setAttribute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMElement::setAttribute

(PHP 5, PHP 7, PHP 8)

DOMElement::setAttribute — Додає новий або змінює існуючий атрибут

### Опис

```methodsynopsis
public DOMElement::setAttribute(string $qualifiedName, string $value): DOMAttr|bool
```

Устанавливает атрибут с именем`qualifiedName`. Якщо атрибут не існує, він буде створений.

### Список параметрів

`qualifiedName`

Ім'я атрибуту.

`value`

Значення атрибуту.

### Значення, що повертаються

Створений чи змінений об'єкт класу [DOMAttr](class.domattr.md)или\*\*`false`\*\*в случае возникновения ошибки.

### Помилки

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**

Виникає, якщо вузол доступний лише читання.

### Приклади

**Приклад #1 Встановлення значення атрибута**

```php
<?php
$doc = new DOMDocument("1.0");
$node = $doc->createElement("para");
$newnode = $doc->appendChild($node);
$newnode->setAttribute("align", "left");
?>
```

### Дивіться також

-   [DOMElement::hasAttribute()](domelement.hasattribute.md) \- Перевіряє, чи існує атрибут
-   [DOMElement::getAttribute()](domelement.getattribute.md) \- Повертає значення атрибуту
-   [DOMElement::removeAttribute()](domelement.removeattribute.md) \- Видаляє атрибут
