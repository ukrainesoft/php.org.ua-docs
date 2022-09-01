---
navigation:
  - domdocument.createelementns.md: '« DOMDocument::createElementNS'
  - domdocument.createprocessinginstruction.md: 'DOMDocument::createProcessingInstruction »'
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::createEntityReference'
---
# DOMDocument::createEntityReference

(PHP 5, PHP 7, PHP 8)

DOMDocument::create Entity Reference — Створити новий вузол посилання на суть

### Опис

```methodsynopsis
public DOMDocument::createEntityReference(string $name): DOMEntityReference|false
```

Ця функція створює екземпляр класу [DOMEntityReference](class.domentityreference.md). Цей вузол не буде відображатися в документі, доки він не буде вставлений, наприклад, функцією [DOMNode::appendChild()](domnode.appendchild.md)

### Список параметрів

`name`

Вміст посилання на сутність, наприклад, посилання на сутність без `&` на початку та `;` в кінці.

### Значення, що повертаються

Новий об'єкт класу [DOMEntityReference](class.domentityreference.md) або **`false`** у разі виникнення помилки.

### Помилки

**`DOM_INVALID_CHARACTER_ERR`**

Виникає, якщо `name` містить неприпустимі символи.

### Дивіться також

-   [DOMNode::appendChild()](domnode.appendchild.md) - Додає новий дочірній вузол до кінця списку нащадків
-   [DOMDocument::createAttribute()](domdocument.createattribute.md) - Створити новий атрибут
-   [DOMDocument::createAttributeNS()](domdocument.createattributens.md) - Створює новий атрибут вузла з відповідним простором імен
-   [DOMDocument::createCDATASection()](domdocument.createcdatasection.md) - Створює новий вузол cdata
-   [DOMDocument::createComment()](domdocument.createcomment.md) - Створити новий вузол коментаря
-   [DOMDocument::createDocumentFragment()](domdocument.createdocumentfragment.md) - створити новий фрагмент документа
-   [DOMDocument::createElement()](domdocument.createelement.md) - Створити новий вузол елемента
-   [DOMDocument::createElementNS()](domdocument.createelementns.md) - Створити новий вузол елемента з відповідним простором імен
-   [DOMDocument::createProcessingInstruction()](domdocument.createprocessinginstruction.md) - Створити новий PI-вузол
-   [DOMDocument::createTextNode()](domdocument.createtextnode.md) - Створити новий текстовий вузол
