Створити новий атрибут

-   [« DOMDocument::construct](domdocument.construct.md)
    
-   [DOMDocument::createAttributeNS »](domdocument.createattributens.md)
    
-   [PHP Manual](index.md)
    
-   [DOMDocument](class.domdocument.md)
    
-   Створити новий атрибут
    

# DOMDocument::createAttribute

(PHP 5, PHP 7, PHP 8)

DOMDocument::createAttribute — Створити новий атрибут

### Опис

```methodsynopsis
public DOMDocument::createAttribute(string $localName): DOMAttr|false
```

Ця функція створює новий об'єкт класу [DOMAttr](class.domattr.md). Цей вузол не буде відображатися в документі, доки він не буде вставлений, наприклад, функцією [DOMNode::appendChild()](domnode.appendchild.md)

### Список параметрів

`localName`

Ім'я атрибуту.

### Значення, що повертаються

Новий об'єкт [DOMAttr](class.domattr.md) або **`false`** у разі виникнення помилки.

### Помилки

**`DOM_INVALID_CHARACTER_ERR`**

Виникає, якщо `localName` містить неприпустимі символи.

### Дивіться також

-   [DOMNode::appendChild()](domnode.appendchild.md) - Додає новий дочірній вузол до кінця списку нащадків
-   [DOMDocument::createAttributeNS()](domdocument.createattributens.md) - Створює новий атрибут вузла з відповідним простором імен
-   [DOMDocument::createCDATASection()](domdocument.createcdatasection.md) - Створює новий вузол cdata
-   [DOMDocument::createComment()](domdocument.createcomment.md) - Створити новий вузол коментаря
-   [DOMDocument::createDocumentFragment()](domdocument.createdocumentfragment.md) - створити новий фрагмент документа
-   [DOMDocument::createElement()](domdocument.createelement.md) - Створити новий вузол елемента
-   [DOMDocument::createElementNS()](domdocument.createelementns.md) - Створити новий вузол елемента з відповідним простором імен
-   [DOMDocument::createEntityReference()](domdocument.createentityreference.md) - Створити новий вузол посилання на суть
-   [DOMDocument::createProcessingInstruction()](domdocument.createprocessinginstruction.md) - Створити новий PI-вузол
-   [DOMDocument::createTextNode()](domdocument.createtextnode.md) - Створити новий текстовий вузол