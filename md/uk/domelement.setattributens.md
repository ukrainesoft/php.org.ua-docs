---
navigation:
  - domelement.setattributenodens.md: '« DOMElement::setAttributeNodeNS'
  - domelement.setidattribute.md: 'DOMElement::setIdAttribute »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::setAttributeNS'
---
# DOMElement::setAttributeNS

(PHP 5, PHP 7, PHP 8)

DOMElement::setAttributeNS — Додає новий атрибут

### Опис

```methodsynopsis
public DOMElement::setAttributeNS(?string $namespace, string $qualifiedName, string $value): void
```

Встановлює атрибут із простором імен `namespace` та локальним ім'ям `name`. Якщо атрибут не існує, його буде створено.

### Список параметрів

`namespace`

URI простір імен.

`qualifiedName`

Кваліфіковане ім'я атрибута у вигляді `prefix:tagname`

`value`

Значення атрибуту.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**

Виникає, якщо вузол доступний лише читання.

**`DOM_NAMESPACE_ERR`**

Виникає, якщо значення `qualifiedName` неправильно, або якщо `qualifiedName` має префікс, а `namespaceURI` **`null`**

### Дивіться також

-   [DOMElement::hasAttributeNS()](domelement.hasattributens.md) - Перевіряє, чи існує заданий атрибут
-   [DOMElement::getAttributeNS()](domelement.getattributens.md) - Повертає значення атрибуту
-   [DOMElement::removeAttributeNS()](domelement.removeattributens.md) - Видаляє атрибут
