---
navigation:
  - domelement.hasattribute.md: '« DOMElement::hasAttribute'
  - domelement.insertadjacentelement.md: 'DOMElement::insertAdjacentElement »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::hasAttributeNS'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMElement::hasAttributeNS

(PHP 5, PHP 7, PHP 8)

DOMElement::hasAttributeNS — Перевіряє, чи існує заданий атрибут

### Опис

```methodsynopsis
public DOMElement::hasAttributeNS(?string $namespace, string $localName): bool
```

Показує, чи існує атрибут у просторі імен `namespace`с именем`localName` у складі елемента.

### Список параметрів

`namespace`

URI простір імен.

`localName`

Місцеве ім'я.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [DOMElement::hasAttribute()](domelement.hasattribute.md) \- Перевіряє, чи існує атрибут
-   [DOMElement::getAttributeNS()](domelement.getattributens.md) \- Повертає значення атрибуту
-   [DOMElement::setAttributeNS()](domelement.setattributens.md) \- Додає новий атрибут
-   [DOMElement::removeAttributeNS()](domelement.removeattributens.md) \- Видаляє атрибут
