---
navigation:
  - domelement.setidattribute.md: '« DOMElement::setIdAttribute'
  - domelement.setidattributens.md: 'DOMElement::setIdAttributeNS »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::setIdAttributeNode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMElement::setIdAttributeNode

(PHP 5, PHP 7, PHP 8)

DOMElement::setIdAttributeNode — Оголошує вказаний атрибут тип ID

### Опис

```methodsynopsis
public DOMElement::setIdAttributeNode(DOMAttr $attr, bool $isId): void
```

Оголошує атрибут, визначений вузлом `attr`, унікальний ідентифікатор елемента.

### Список параметрів

`attr`

Вузол атрибуту.

`isId`

Параметр устанавливают в\*\*`true`\*\*якщо потрібно, щоб тип переданого атрибута з ім'ям `name` став ідентифікатором елемента, інакше вказують **`false`**

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**

Виникає, якщо вузол доступний лише читання.

**`DOM_NOT_FOUND`**

Виникає, якщо атрибут з ім'ям `name` не належить елементу.

### Дивіться також

-   [DOMDocument::getElementById()](domdocument.getelementbyid.md) \- Шукає елемент із певним ідентифікатором
-   [DOMElement::setIdAttribute()](domelement.setidattribute.md) \- Оголошує атрибуту із зазначеним ім'ям тип ID
-   [DOMElement::setIdAttributeNS()](domelement.setidattributens.md) \- Оголошує атрибуту із зазначеними локальним ім'ям та URI простору імен тип ID
