Створити новий фрагмент документа

-   [« DOMDocument::createComment](domdocument.createcomment.html)
    
-   [DOMDocument::createElement »](domdocument.createelement.html)
    
-   [PHP Manual](index.html)
    
-   [DOMDocument](class.domdocument.html)
    
-   Створити новий фрагмент документа
    

# DOMDocument::createDocumentFragment

(PHP 5, PHP 7, PHP 8)

DOMDocument::createDocumentFragment — Створити новий фрагмент документа

### Опис

```methodsynopsis
public DOMDocument::createDocumentFragment(): DOMDocumentFragment
```

Ця функція створює новий екземпляр класу [DOMDocumentFragment](class.domdocumentfragment.html). Цей вузол не буде відображатися в документі, доки він не буде вставлений, наприклад, функцією [DOMNode::appendChild()](domnode.appendchild.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Новий об'єкт класу [DOMDocumentFragment](class.domdocumentfragment.html)

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі виникнення помилки тепер викидає виняток [DomException](class.domexception.html). Раніше натомість поверталося значення **`false`** |

### Дивіться також

-   [DOMNode::appendChild()](domnode.appendchild.html) - Додає новий дочірній вузол до кінця списку нащадків
-   [DOMDocument::createAttribute()](domdocument.createattribute.html) - Створити новий атрибут
-   [DOMDocument::createAttributeNS()](domdocument.createattributens.html) - Створює новий атрибут вузла з відповідним простором імен
-   [DOMDocument::createCDATASection()](domdocument.createcdatasection.html) - Створює новий вузол cdata
-   [DOMDocument::createComment()](domdocument.createcomment.html) - Створити новий вузол коментаря
-   [DOMDocument::createElement()](domdocument.createelement.html) - Створити новий вузол елемента
-   [DOMDocument::createElementNS()](domdocument.createelementns.html) - Створити новий вузол елемента з відповідним простором імен
-   [DOMDocument::createEntityReference()](domdocument.createentityreference.html) - Створити новий вузол посилання на суть
-   [DOMDocument::createProcessingInstruction()](domdocument.createprocessinginstruction.html) - Створити новий PI-вузол
-   [DOMDocument::createTextNode()](domdocument.createtextnode.html) - Створити новий текстовий вузол