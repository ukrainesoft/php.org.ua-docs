---
navigation:
  - domelement.construct.md: '« DOMElement::\_\_construct'
  - domelement.getattributenames.md: 'DOMElement::getAttributeNames »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::getAttribute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMElement::getAttribute

(PHP 5, PHP 7, PHP 8)

DOMElement::getAttribute — Повертає значення атрибуту

### Опис

```methodsynopsis
public DOMElement::getAttribute(string $qualifiedName): string
```

Возвращает значение атрибута с именем`qualifiedName` для поточного сайту.

### Список параметрів

`qualifiedName`

Ім'я атрибуту.

### Значення, що повертаються

Значення атрибута або пусте значення, якщо атрибут із вказаним ім'ям `qualifiedName`не найден.

### Дивіться також

-   [DOMElement::hasAttribute()](domelement.hasattribute.md) \- Перевіряє, чи існує атрибут
-   [DOMElement::setAttribute()](domelement.setattribute.md) \- Додає новий або змінює існуючий атрибут
-   [DOMElement::removeAttribute()](domelement.removeattribute.md) \- Видаляє атрибут
