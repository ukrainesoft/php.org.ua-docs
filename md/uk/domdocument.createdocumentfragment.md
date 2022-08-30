Створити новий фрагмент документа

-   [« DOMDocument::createComment](domdocument.createcomment.md)
    
-   [DOMDocument::createElement »](domdocument.createelement.md)
    
-   [PHP Manual](index.md)
    
-   [DOMDocument](class.domdocument.md)
    
-   Створити новий фрагмент документа
    

# DOMDocument::createDocumentFragment

(PHP 5, PHP 7, PHP 8)

DOMDocument::createDocumentFragment — Створити новий фрагмент документа

### Опис

```methodsynopsis
public DOMDocument::createDocumentFragment(): DOMDocumentFragment
```

Ця функція створює новий екземпляр класу [DOMDocumentFragment](class.domdocumentfragment.md). Цей вузол не буде відображатися в документі, доки він не буде вставлений, наприклад, функцією [DOMNode::appendChild()](domnode.appendchild.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Новий об'єкт класу [DOMDocumentFragment](class.domdocumentfragment.md)

### список змін

| Версия | Описание                                                                                                                                 |
|--------|------------------------------------------------------------------------------------------------------------------------------------------|
|        | У разі виникнення помилки тепер викидає виняток [DomException](class.domexception.md). Раніше натомість поверталося значення **`false`** |

### Дивіться також

-   [DOMNode::appendChild()](domnode.appendchild.md) - Додає новий дочірній вузол до кінця списку нащадків
-   [DOMDocument::createAttribute()](domdocument.createattribute.md) - Створити новий атрибут
-   [DOMDocument::createAttributeNS()](domdocument.createattributens.md) - Створює новий атрибут вузла з відповідним простором імен
-   [DOMDocument::createCDATASection()](domdocument.createcdatasection.md) - Створює новий вузол cdata
-   [DOMDocument::createComment()](domdocument.createcomment.md) - Створити новий вузол коментаря
-   [DOMDocument::createElement()](domdocument.createelement.md) - Створити новий вузол елемента
-   [DOMDocument::createElementNS()](domdocument.createelementns.md) - Створити новий вузол елемента з відповідним простором імен
-   [DOMDocument::createEntityReference()](domdocument.createentityreference.md) - Створити новий вузол посилання на суть
-   [DOMDocument::createProcessingInstruction()](domdocument.createprocessinginstruction.md) - Створити новий PI-вузол
-   [DOMDocument::createTextNode()](domdocument.createtextnode.md) - Створити новий текстовий вузол