---
navigation:
  - domdocument.createattribute.md: '« DOMDocument::createAttribute'
  - domdocument.createcdatasection.md: 'DOMDocument::createCDATASection »'
  - index.md: PHP Manual
  - class.domdocument.md: DOMDocument
title: 'DOMDocument::createAttributeNS'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMDocument::createAttributeNS

(PHP 5, PHP 7, PHP 8)

DOMDocument::createAttributeNS — Створює новий атрибут вузла з відповідним простором імен

### Опис

```methodsynopsis
public DOMDocument::createAttributeNS(?string $namespace, string $qualifiedName): DOMAttr|false
```

Ця функція створює новий об'єкт класу [DOMAttr](class.domattr.md). Цей вузол не відображатиметься в документі, доки він не буде вставлений, наприклад, функцією [DOMNode::appendChild()](domnode.appendchild.md)

### Список параметрів

`namespace`

URI простір імен.

`qualifiedName`

Ім'я та префікс атрибуту у вигляді `prefix:tagname`

### Значення, що повертаються

Новий екземпляр класу [DOMAttr](class.domattr.md)или\*\*`false`\*\*в случае ошибки.

### Помилки

**`DOM_INVALID_CHARACTER_ERR`**

Виникає, якщо `qualifiedName` містить неприпустимі символи.

**`DOM_NAMESPACE_ERR`**

Виникає, якщо `qualifiedName` неправильно сформовано, або якщо `qualifiedName`имеет префикс, а`namespace`имеет значение\*\*`null`\*\*

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Виклик цього методу без вказівки префікса тепер вибере префікс замість того, щоб використовувати простір імен за замовчуванням. Раніше це створювало атрибут без префікса і неправильно застосовувало простір імен до елемента-власника, оскільки простори стандартних імен не застосовуються до атрибутів. |
| 8.3.0 | Виклик цього методу з префіксом, який вже був оголошений на елементі-власника з іншим URI простору імен, тепер змінить новий префікс, щоб уникнути створення конфліктів простору імен. Це призводить поведінку у відповідність до специфікації DOM. Previously this threw a [DOMException](class.domexception.md) with code **`DOM_NAMESPACE_ERR`** |

### Дивіться також

-   [DOMNode::appendChild()](domnode.appendchild.md) \- Додає новий дочірній вузол до кінця списку нащадків
-   [DOMDocument::createAttribute()](domdocument.createattribute.md) \- Створює новий атрибут
-   [DOMDocument::createCDATASection()](domdocument.createcdatasection.md) \- Створює новий вузол cdata
-   [DOMDocument::createComment()](domdocument.createcomment.md) \- Створити новий вузол коментаря
-   [DOMDocument::createDocumentFragment()](domdocument.createdocumentfragment.md) \- Створює новий фрагмент документа
-   [DOMDocument::createElement()](domdocument.createelement.md) \- Створює новий вузол елемента
-   [DOMDocument::createElementNS()](domdocument.createelementns.md) \- Створити новий вузол елемента з відповідним простором імен
-   [DOMDocument::createEntityReference()](domdocument.createentityreference.md) \- Створити новий вузол посилання на суть
-   [DOMDocument::createProcessingInstruction()](domdocument.createprocessinginstruction.md) \- Створити новий PI-вузол
-   [DOMDocument::createTextNode()](domdocument.createtextnode.md) \- Створити новий текстовий вузол
