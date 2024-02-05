---
navigation:
  - domelement.remove.md: '« DOMElement::remove'
  - domelement.removeattributenode.md: 'DOMElement::removeAttributeNode »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::removeAttribute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMElement::removeAttribute

(PHP 5, PHP 7, PHP 8)

DOMElement::removeAttribute — Видаляє атрибут

### Опис

```methodsynopsis
public DOMElement::removeAttribute(string $qualifiedName): bool
```

Удаляет атрибут с именем`qualifiedName` елемент.

### Список параметрів

`qualifiedName`

Ім'я атрибуту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**

Виникає, якщо атрибут доступний лише для читання.

### Дивіться також

-   [DOMElement::hasAttribute()](domelement.hasattribute.md) \- Перевіряє, чи існує атрибут
-   [DOMElement::getAttribute()](domelement.getattribute.md) \- Повертає значення атрибуту
-   [DOMElement::setAttribute()](domelement.setattribute.md) \- Додає новий або змінює існуючий атрибут
