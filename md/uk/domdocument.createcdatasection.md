Створює новий вузол cdata

-   [« DOMDocument::createAttributeNS](domdocument.createattributens.html)
    
-   [DOMDocument::createComment »](domdocument.createcomment.html)
    
-   [PHP Manual](index.html)
    
-   [DOMDocument](class.domdocument.html)
    
-   Створює новий вузол cdata
    

# DOMDocument::createCDATASection

(PHP 5, PHP 7, PHP 8)

DOMDocument::createCDATASection — Створює новий вузол cdata

### Опис

```methodsynopsis
public DOMDocument::createCDATASection(string $data): DOMCdataSection|false
```

Ця функція створює новий об'єкт класу [DOMCDATASection](class.domcdatasection.html). Цей вузол не буде відображатися в документі, доки він не буде вставлений, наприклад, функцією [DOMNode::appendChild()](domnode.appendchild.html)

### Список параметрів

`data`

Вміст cdata.

### Значення, що повертаються

Новий об'єкт класу [DOMCDATASection](class.domcdatasection.html) або **`false`** у разі виникнення помилки.

### Дивіться також

-   [DOMNode::appendChild()](domnode.appendchild.html) - Додає новий дочірній вузол до кінця списку нащадків
-   [DOMDocument::createAttribute()](domdocument.createattribute.html) - Створити новий атрибут
-   [DOMDocument::createAttributeNS()](domdocument.createattributens.html) - Створює новий атрибут вузла з відповідним простором імен
-   [DOMDocument::createComment()](domdocument.createcomment.html) - Створити новий вузол коментаря
-   [DOMDocument::createDocumentFragment()](domdocument.createdocumentfragment.html) - створити новий фрагмент документа
-   [DOMDocument::createElement()](domdocument.createelement.html) - Створити новий вузол елемента
-   [DOMDocument::createElementNS()](domdocument.createelementns.html) - Створити новий вузол елемента з відповідним простором імен
-   [DOMDocument::createEntityReference()](domdocument.createentityreference.html) - Створити новий вузол посилання на суть
-   [DOMDocument::createProcessingInstruction()](domdocument.createprocessinginstruction.html) - Створити новий PI-вузол
-   [DOMDocument::createTextNode()](domdocument.createtextnode.html) - Створити новий текстовий вузол