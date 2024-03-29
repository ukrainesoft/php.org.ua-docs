---
navigation:
  - domelement.getelementsbytagnamens.md: '« DOMElement::getElementsByTagNameNS'
  - domelement.hasattributens.md: 'DOMElement::hasAttributeNS »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::hasAttribute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMElement::hasAttribute

(PHP 5, PHP 7, PHP 8)

DOMElement::hasAttribute — Перевіряє, чи існує атрибут

### Опис

```methodsynopsis
public DOMElement::hasAttribute(string $qualifiedName): bool
```

Перевіряє наявність атрибута з ім'ям, вказаним у параметрі `qualifiedName` поточний елемент.

### Список параметрів

`qualifiedName`

Ім'я атрибуту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [DOMElement::hasAttributeNS()](domelement.hasattributens.md) \- Перевіряє, чи існує заданий атрибут
-   [DOMElement::getAttribute()](domelement.getattribute.md) \- Повертає значення атрибуту
-   [DOMElement::setAttribute()](domelement.setattribute.md) \- Додає новий або змінює існуючий атрибут
-   [DOMElement::removeAttribute()](domelement.removeattribute.md) \- Видаляє атрибут
