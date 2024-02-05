---
navigation:
  - domdocument.createcomment.md: '« DOMDocument::createComment'
  - domdocument.createelement.md: 'DOMDocument::createElement »'
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::createDocumentFragment'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMDocument::createDocumentFragment

(PHP 5, PHP 7, PHP 8)

DOMDocument::createDocumentFragment — Створює новий фрагмент документу

### Опис

```methodsynopsis
public DOMDocument::createDocumentFragment(): DOMDocumentFragment
```

Ця функція створює новий екземпляр класу [DOMDocumentFragment](class.domdocumentfragment.md). Цей вузол не відображатиметься в документі, доки він не буде вставлений, наприклад, функцією [DOMNode::appendChild()](domnode.appendchild.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає новий об'єкт класу [DOMDocumentFragment](class.domdocumentfragment.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | У разі виникнення помилки тепер викидає виняток [DomException](class.domexception.md). . Раніше натомість поверталося значення **`false`** |

### Дивіться також

-   [DOMNode::appendChild()](domnode.appendchild.md) \- Додає новий дочірній вузол до кінця списку нащадків
-   [DOMDocument::createAttribute()](domdocument.createattribute.md) \- Створює новий атрибут
-   [DOMDocument::createAttributeNS()](domdocument.createattributens.md) \- Створює новий атрибут вузла з відповідним простором імен
-   [DOMDocument::createCDATASection()](domdocument.createcdatasection.md) \- Створює новий вузол cdata
-   [DOMDocument::createComment()](domdocument.createcomment.md) \- Створити новий вузол коментаря
-   [DOMDocument::createElement()](domdocument.createelement.md) \- Створює новий вузол елемента
-   [DOMDocument::createElementNS()](domdocument.createelementns.md) \- Створити новий вузол елемента з відповідним простором імен
-   [DOMDocument::createEntityReference()](domdocument.createentityreference.md) \- Створити новий вузол посилання на суть
-   [DOMDocument::createProcessingInstruction()](domdocument.createprocessinginstruction.md) \- Створити новий PI-вузол
-   [DOMDocument::createTextNode()](domdocument.createtextnode.md) \- Створити новий текстовий вузол
