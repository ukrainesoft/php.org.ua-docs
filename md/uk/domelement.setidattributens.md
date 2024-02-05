---
navigation:
  - domelement.setidattributenode.md: '« DOMElement::setIdAttributeNode'
  - domelement.toggleattribute.md: 'DOMElement::toggleAttribute »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::setIdAttributeNS'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMElement::setIdAttributeNS

(PHP 5, PHP 7, PHP 8)

DOMElement::setIdAttributeNS — Оголошує атрибут з вказаними локальним ім'ям і URI простору імен тип ID

### Опис

```methodsynopsis
public DOMElement::setIdAttributeNS(string $namespace, string $qualifiedName, bool $isId): void
```

Оголошує атрибут із зазначеним кваліфікованим ім'ям `qualifiedName` та простором імен `namespace` унікальний ідентифікатор елемента.

### Список параметрів

`namespace`

URI простір імен атрибута.

`qualifiedName`

Локальное имя атрибута в виде`prefix:tagname`

`isId`

Параметр устанавливают в\*\*`true`\*\*якщо потрібно, щоб тип атрибута з ім'ям `name` став ідентифікатором елемента, інакше вказують **`false`**

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
-   [DOMElement::setIdAttributeNode()](domelement.setidattributenode.md) \- Оголошує вказаний вузл атрибута тип ID
