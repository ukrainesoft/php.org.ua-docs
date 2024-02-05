---
navigation:
  - domdocument.createelementns.md: '« DOMDocument::createElementNS'
  - domdocument.createprocessinginstruction.md: 'DOMDocument::createProcessingInstruction »'
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::createEntityReference'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMDocument::createEntityReference

(PHP 5, PHP 7, PHP 8)

DOMDocument::createEntityReference — Створити новий вузол посилання на суть

### Опис

```methodsynopsis
public DOMDocument::createEntityReference(string $name): DOMEntityReference|false
```

Ця функція створює екземпляр класу [DOMEntityReference](class.domentityreference.md). Цей вузол не відображатиметься в документі, доки він не буде вставлений, наприклад, функцією [DOMNode::appendChild()](domnode.appendchild.md)

### Список параметрів

`name`

Вміст посилання на сутність, наприклад, посилання на сутність без `&`в начале и в кінці.

### Значення, що повертаються

Новий об'єкт класу [DOMEntityReference](class.domentityreference.md)или\*\*`false`\*\*в случае возникновения ошибки.

### Помилки

**`DOM_INVALID_CHARACTER_ERR`**

Виникає, якщо `name` містить неприпустимі символи.

### Дивіться також

-   [DOMNode::appendChild()](domnode.appendchild.md) \- Додає новий дочірній вузол до кінця списку нащадків
-   [DOMDocument::createAttribute()](domdocument.createattribute.md) \- Створює новий атрибут
-   [DOMDocument::createAttributeNS()](domdocument.createattributens.md) \- Створює новий атрибут вузла з відповідним простором імен
-   [DOMDocument::createCDATASection()](domdocument.createcdatasection.md) \- Створює новий вузол cdata
-   [DOMDocument::createComment()](domdocument.createcomment.md) \- Створити новий вузол коментаря
-   [DOMDocument::createDocumentFragment()](domdocument.createdocumentfragment.md) \- Створює новий фрагмент документа
-   [DOMDocument::createElement()](domdocument.createelement.md) \- Створює новий вузол елемента
-   [DOMDocument::createElementNS()](domdocument.createelementns.md) \- Створити новий вузол елемента з відповідним простором імен
-   [DOMDocument::createProcessingInstruction()](domdocument.createprocessinginstruction.md) \- Створити новий PI-вузол
-   [DOMDocument::createTextNode()](domdocument.createtextnode.md) \- Створити новий текстовий вузол
