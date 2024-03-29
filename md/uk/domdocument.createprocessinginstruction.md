---
navigation:
  - domdocument.createentityreference.md: '« DOMDocument::createEntityReference'
  - domdocument.createtextnode.md: 'DOMDocument::createTextNode »'
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::createProcessingInstruction'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMDocument::createProcessingInstruction

(PHP 5, PHP 7, PHP 8)

DOMDocument::createProcessingInstruction — Створити новий PI-сайт

### Опис

```methodsynopsis
public DOMDocument::createProcessingInstruction(string $target, string $data = ""): DOMProcessingInstruction|false
```

Ця функція створює екземпляр класу [DOMProcessingInstruction](class.domprocessinginstruction.md). Цей вузол не відображатиметься в документі, доки він не буде вставлений, наприклад, функцією [DOMNode::appendChild()](domnode.appendchild.md)

### Список параметрів

`target`

Ціль інструкції для обробника документа.

`data`

Вміст інструкції оброблювача.

### Значення, що повертаються

Новий об'єкт класу [DOMProcessingInstruction](class.domprocessinginstruction.md)либо\*\*`false`\*\*в случае возникновения ошибки.

### Помилки

**`DOM_INVALID_CHARACTER_ERR`**

Виникає, якщо `target` містить неприпустимі символи.

### Дивіться також

-   [DOMNode::appendChild()](domnode.appendchild.md) \- Додає новий дочірній вузол до кінця списку нащадків
-   [DOMDocument::createAttribute()](domdocument.createattribute.md) \- Створює новий атрибут
-   [DOMDocument::createAttributeNS()](domdocument.createattributens.md) \- Створює новий атрибут вузла з відповідним простором імен
-   [DOMDocument::createCDATASection()](domdocument.createcdatasection.md) \- Створює новий вузол cdata
-   [DOMDocument::createComment()](domdocument.createcomment.md) \- Створити новий вузол коментаря
-   [DOMDocument::createDocumentFragment()](domdocument.createdocumentfragment.md) \- Створює новий фрагмент документа
-   [DOMDocument::createElement()](domdocument.createelement.md) \- Створює новий вузол елемента
-   [DOMDocument::createElementNS()](domdocument.createelementns.md) \- Створити новий вузол елемента з відповідним простором імен
-   [DOMDocument::createEntityReference()](domdocument.createentityreference.md) \- Створити новий вузол посилання на суть
-   [DOMDocument::createTextNode()](domdocument.createtextnode.md) \- Створити новий текстовий вузол
