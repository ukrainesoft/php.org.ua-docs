---
navigation:
  - domdocument.construct.md: '« DOMDocument::\_\_construct'
  - domdocument.createattributens.md: 'DOMDocument::createAttributeNS »'
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::createAttribute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMDocument::createAttribute

(PHP 5, PHP 7, PHP 8)

DOMDocument::createAttribute — Створює новий атрибут

### Опис

```methodsynopsis
public DOMDocument::createAttribute(string $localName): DOMAttr|false
```

Ця функція створює новий об'єкт класу [DOMAttr](class.domattr.md). Цей вузол не відображатиметься в документі, доки він не буде вставлений, наприклад, функцією [DOMNode::appendChild()](domnode.appendchild.md)

### Список параметрів

`localName`

Ім'я атрибуту.

### Значення, що повертаються

Повертає новий об'єкт [DOMAttr](class.domattr.md)либо\*\*`false`\*\*в случае возникновения ошибки.

### Помилки

**`DOM_INVALID_CHARACTER_ERR`**

Виникає, якщо параметр `localName` містить неприпустимі символи.

### Дивіться також

-   [DOMNode::appendChild()](domnode.appendchild.md) \- Додає новий дочірній вузол до кінця списку нащадків
-   [DOMDocument::createAttributeNS()](domdocument.createattributens.md) \- Створює новий атрибут вузла з відповідним простором імен
-   [DOMDocument::createCDATASection()](domdocument.createcdatasection.md) \- Створює новий вузол cdata
-   [DOMDocument::createComment()](domdocument.createcomment.md) \- Створити новий вузол коментаря
-   [DOMDocument::createDocumentFragment()](domdocument.createdocumentfragment.md) \- Створює новий фрагмент документа
-   [DOMDocument::createElement()](domdocument.createelement.md) \- Створює новий вузол елемента
-   [DOMDocument::createElementNS()](domdocument.createelementns.md) \- Створити новий вузол елемента з відповідним простором імен
-   [DOMDocument::createEntityReference()](domdocument.createentityreference.md) \- Створити новий вузол посилання на суть
-   [DOMDocument::createProcessingInstruction()](domdocument.createprocessinginstruction.md) \- Створити новий PI-вузол
-   [DOMDocument::createTextNode()](domdocument.createtextnode.md) \- Створити новий текстовий вузол
