---
navigation:
  - domelement.setattributens.md: '« DOMElement::setAttributeNS'
  - domelement.setidattributenode.md: 'DOMElement::setIdAttributeNode »'
  - index.md: PHP Manual
  - class.domelement.md: DOMElement
title: 'DOMElement::setIdAttribute'
---
# DOMElement::setIdAttribute

(PHP 5, PHP 7, PHP 8)

DOMElement::setIdAttribute — Оголошує атрибут, вказаний ім'ям, з ідентифікатором типу

### Опис

```methodsynopsis
public DOMElement::setIdAttribute(string $qualifiedName, bool $isId): void
```

Оголошує атрибут `qualifiedName` з ідентифікатором типу

### Список параметрів

`qualifiedName`

Ім'я атрибуту.

`isId`

Встановіть значення в **`true`** якщо ви хочете, щоб `qualifiedName` мав ідентифікатор типу, **`false`** в іншому випадку.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**

Виникає, якщо вузол доступний лише читання.

**`DOM_NOT_FOUND`**

Виникає, якщо `qualifiedName` не є атрибутом елемента.

### Дивіться також

-   [DOMDocument::getElementById()](domdocument.getelementbyid.md) - Шукає елемент із певним ідентифікатором
-   [DOMElement::setIdAttributeNode()](domelement.setidattributenode.md) - Оголошує атрибут, вказаний вузлом, з ідентифікатором типу
-   [DOMElement::setIdAttributeNS()](domelement.setidattributens.md) - Оголошує атрибут, вказаний локальним ім'ям та URI простору імен, з ідентифікатором типу
