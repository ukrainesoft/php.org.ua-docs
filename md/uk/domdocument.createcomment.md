---
navigation:
  - domdocument.createcdatasection.md: '« DOMDocument::createCDATASection'
  - domdocument.createdocumentfragment.md: 'DOMDocument::createDocumentFragment »'
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::createComment'
---
# DOMDocument::createComment

(PHP 5, PHP 7, PHP 8)

DOMDocument::createComment — Створити новий вузол коментаря

### Опис

```methodsynopsis
public DOMDocument::createComment(string $data): DOMComment
```

Ця функція створює новий екземпляр класу [DOMComment](class.domcomment.md). Цей вузол не відображатиметься в документі, доки він не буде вставлений, наприклад, функцією [DOMNode::appendChild()](domnode.appendchild.md)

### Список параметрів

`data`

Зміст коментаря.

### Значення, що повертаються

Новий об'єкт класу [DOMComment](class.domcomment.md)

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі виникнення помилки тепер викидає виняток [DomException](class.domexception.md). Раніше натомість поверталося значення **`false`** |

### Дивіться також

-   [DOMNode::appendChild()](domnode.appendchild.md) - Додає новий дочірній вузол до кінця списку нащадків
-   [DOMDocument::createAttribute()](domdocument.createattribute.md) - Створити новий атрибут
-   [DOMDocument::createAttributeNS()](domdocument.createattributens.md) - Створює новий атрибут вузла з відповідним простором імен
-   [DOMDocument::createCDATASection()](domdocument.createcdatasection.md) - Створює новий вузол cdata
-   [DOMDocument::createDocumentFragment()](domdocument.createdocumentfragment.md) - створити новий фрагмент документа
-   [DOMDocument::createElement()](domdocument.createelement.md) - Створити новий вузол елемента
-   [DOMDocument::createElementNS()](domdocument.createelementns.md) - Створити новий вузол елемента з відповідним простором імен
-   [DOMDocument::createEntityReference()](domdocument.createentityreference.md) - Створити новий вузол посилання на суть
-   [DOMDocument::createProcessingInstruction()](domdocument.createprocessinginstruction.md) - Створити новий PI-вузол
-   [DOMDocument::createTextNode()](domdocument.createtextnode.md) - Створити новий текстовий вузол
