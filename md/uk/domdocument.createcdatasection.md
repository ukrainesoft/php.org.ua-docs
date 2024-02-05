---
navigation:
  - domdocument.createattributens.md: '« DOMDocument::createAttributeNS'
  - domdocument.createcomment.md: 'DOMDocument::createComment »'
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::createCDATASection'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMDocument::createCDATASection

(PHP 5, PHP 7, PHP 8)

DOMDocument::createCDATASection — Створює новий вузол cdata

### Опис

```methodsynopsis
public DOMDocument::createCDATASection(string $data): DOMCdataSection|false
```

Ця функція створює новий об'єкт класу [DOMCDATASection](class.domcdatasection.md). Цей вузол не відображатиметься в документі, доки він не буде вставлений, наприклад, функцією [DOMNode::appendChild()](domnode.appendchild.md)

### Список параметрів

`data`

Вміст cdata.

### Значення, що повертаються

Новий об'єкт класу [DOMCDATASection](class.domcdatasection.md)или\*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [DOMNode::appendChild()](domnode.appendchild.md) \- Додає новий дочірній вузол до кінця списку нащадків
-   [DOMDocument::createAttribute()](domdocument.createattribute.md) \- Створює новий атрибут
-   [DOMDocument::createAttributeNS()](domdocument.createattributens.md) \- Створює новий атрибут вузла з відповідним простором імен
-   [DOMDocument::createComment()](domdocument.createcomment.md) \- Створити новий вузол коментаря
-   [DOMDocument::createDocumentFragment()](domdocument.createdocumentfragment.md) \- Створює новий фрагмент документа
-   [DOMDocument::createElement()](domdocument.createelement.md) \- Створює новий вузол елемента
-   [DOMDocument::createElementNS()](domdocument.createelementns.md) \- Створити новий вузол елемента з відповідним простором імен
-   [DOMDocument::createEntityReference()](domdocument.createentityreference.md) \- Створити новий вузол посилання на суть
-   [DOMDocument::createProcessingInstruction()](domdocument.createprocessinginstruction.md) \- Створити новий PI-вузол
-   [DOMDocument::createTextNode()](domdocument.createtextnode.md) \- Створити новий текстовий вузол
