Створити новий текстовий вузол

-   [« DOMDocument::createProcessingInstruction](domdocument.createprocessinginstruction.html)
    
-   [DOMDocument::getElementById »](domdocument.getelementbyid.html)
    
-   [PHP Manual](index.html)
    
-   [DOMDocument](class.domdocument.html)
    
-   Створити новий текстовий вузол
    

# DOMDocument::createTextNode

(PHP 5, PHP 7, PHP 8)

DOMDocument::createTextNode — Створити новий текстовий вузол

### Опис

```methodsynopsis
public DOMDocument::createTextNode(string $data): DOMText
```

Ця функція створює екземпляр класу [DOMText](class.domtext.html). Цей вузол не відображатиметься в документі, доки він не буде вставлений, наприклад, функцією [DOMNode::appendChild()](domnode.appendchild.html)

### Список параметрів

`data`

Вміст вузла.

### Значення, що повертаються

Повертає новий об'єкт класу [DOMText](class.domtext.html)

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
-   [DOMDocument::createDocumentFragment()](domdocument.createdocumentfragment.html) - створити новий фрагмент документа
-   [DOMDocument::createElement()](domdocument.createelement.html) - Створити новий вузол елемента
-   [DOMDocument::createElementNS()](domdocument.createelementns.html) - Створити новий вузол елемента з відповідним простором імен
-   [DOMDocument::createEntityReference()](domdocument.createentityreference.html) - Створити новий вузол посилання на суть
-   [DOMDocument::createProcessingInstruction()](domdocument.createprocessinginstruction.html) - Створити новий PI-вузол