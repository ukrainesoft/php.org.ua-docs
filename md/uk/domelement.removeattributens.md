---
navigation:
  - domelement.removeattributenode.md: '« DOMElement::removeAttributeNode'
  - domelement.replacechildren.md: 'DOMElement::replaceChildren »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::removeAttributeNS'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMElement::removeAttributeNS

(PHP 5, PHP 7, PHP 8)

DOMElement::removeAttributeNS — Видаляє атрибут

### Опис

```methodsynopsis
public DOMElement::removeAttributeNS(?string $namespace, string $localName): void
```

Удаляет атрибут`localName` у просторі імен `namespace` елемент.

### Список параметрів

`namespace`

URI простір імен.

`localName`

Місцеве ім'я.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**

Виникає, якщо вузол доступний лише читання.

### Дивіться також

-   [DOMElement::hasAttributeNS()](domelement.hasattributens.md) \- Перевіряє, чи існує заданий атрибут
-   [DOMElement::getAttributeNS()](domelement.getattributens.md) \- Повертає значення атрибуту
-   [DOMElement::setAttributeNS()](domelement.setattributens.md) \- Додає новий атрибут
