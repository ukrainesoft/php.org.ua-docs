Створити новий вузол коментаря

-   [« DOMDocument::createCDATASection](domdocument.createcdatasection.html)
    
-   [DOMDocument::createDocumentFragment »](domdocument.createdocumentfragment.html)
    
-   [PHP Manual](index.html)
    
-   [DOMDocument](class.domdocument.html)
    
-   Створити новий вузол коментаря
    

# DOMDocument::createComment

(PHP 5, PHP 7, PHP 8)

DOMDocument::createComment — Створити новий вузол коментаря

### Опис

```methodsynopsis
public DOMDocument::createComment(string $data): DOMComment
```

Ця функція створює новий екземпляр класу [DOMComment](class.domcomment.html). Цей вузол не відображатиметься в документі, доки він не буде вставлений, наприклад, функцією [DOMNode::appendChild()](domnode.appendchild.html)

### Список параметрів

`data`

Зміст коментаря.

### Значення, що повертаються

Новий об'єкт класу [DOMComment](class.domcomment.html)

### список змін

| Версия | Описание                                                                                                                                   |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------|
|        | У разі виникнення помилки тепер викидає виняток [DomException](class.domexception.html). Раніше натомість поверталося значення **`false`** |

### Дивіться також

-   [DOMNode::appendChild()](domnode.appendchild.html) - Додає новий дочірній вузол до кінця списку нащадків
-   [DOMDocument::createAttribute()](domdocument.createattribute.html) - Створити новий атрибут
-   [DOMDocument::createAttributeNS()](domdocument.createattributens.html) - Створює новий атрибут вузла з відповідним простором імен
-   [DOMDocument::createCDATASection()](domdocument.createcdatasection.html) - Створює новий вузол cdata
-   [DOMDocument::createDocumentFragment()](domdocument.createdocumentfragment.html) - створити новий фрагмент документа
-   [DOMDocument::createElement()](domdocument.createelement.html) - Створити новий вузол елемента
-   [DOMDocument::createElementNS()](domdocument.createelementns.html) - Створити новий вузол елемента з відповідним простором імен
-   [DOMDocument::createEntityReference()](domdocument.createentityreference.html) - Створити новий вузол посилання на суть
-   [DOMDocument::createProcessingInstruction()](domdocument.createprocessinginstruction.html) - Створити новий PI-вузол
-   [DOMDocument::createTextNode()](domdocument.createtextnode.html) - Створити новий текстовий вузол