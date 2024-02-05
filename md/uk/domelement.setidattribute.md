---
navigation:
  - domelement.setattributens.md: '« DOMElement::setAttributeNS'
  - domelement.setidattributenode.md: 'DOMElement::setIdAttributeNode »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::setIdAttribute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMElement::setIdAttribute

(PHP 5, PHP 7, PHP 8)

DOMElement::setIdAttribute — Оголошує атрибут із зазначеним ім'ям тип ID

### Опис

```methodsynopsis
public DOMElement::setIdAttribute(string $qualifiedName, bool $isId): void
```

Оголошує атрибут із кваліфікованим ім'ям `qualifiedName` унікальний ідентифікатор елемента.

### Список параметрів

`qualifiedName`

Ім'я атрибуту.

`isId`

Параметр устанавливают в\*\*`true`\*\*, якщо потрібно, щоб тип атрибута, ім'я якого вказано у параметрі `qualifiedName`, став ідентифікатором елемента, інакше вказують **`false`**

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**

Виникає, якщо вузол доступний лише читання.

**`DOM_NOT_FOUND`**

Виникає, якщо ім'я `qualifiedName` не належить елементу.

### Дивіться також

-   [DOMDocument::getElementById()](domdocument.getelementbyid.md) \- Шукає елемент із певним ідентифікатором
-   [DOMElement::setIdAttributeNode()](domelement.setidattributenode.md) \- Оголошує вказаний вузл атрибута тип ID
-   [DOMElement::setIdAttributeNS()](domelement.setidattributens.md) \- Оголошує атрибуту із зазначеними локальним ім'ям та URI простору імен тип ID
