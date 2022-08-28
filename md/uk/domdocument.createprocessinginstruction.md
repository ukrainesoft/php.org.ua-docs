Створити новий PI-вузол

-   [« DOMDocument::createEntityReference](domdocument.createentityreference.html)
    
-   [DOMDocument::createTextNode »](domdocument.createtextnode.html)
    
-   [PHP Manual](index.html)
    
-   [DOMDocument](class.domdocument.html)
    
-   Створити новий PI-вузол
    

# DOMDocument::createProcessingInstruction

(PHP 5, PHP 7, PHP 8)

DOMDocument::createProcessingInstruction — Створити новий PI-сайт

### Опис

```methodsynopsis
public DOMDocument::createProcessingInstruction(string $target, string $data = ""): DOMProcessingInstruction|false
```

Ця функція створює екземпляр класу [DOMProcessingInstruction](class.domprocessinginstruction.html). Цей вузол не буде відображатися в документі, доки він не буде вставлений, наприклад, функцією [DOMNode::appendChild()](domnode.appendchild.html)

### Список параметрів

`target`

Ціль інструкції для обробника документа.

`data`

Вміст інструкції оброблювача.

### Значення, що повертаються

Новий об'єкт класу [DOMProcessingInstruction](class.domprocessinginstruction.html) або **`false`** у разі виникнення помилки.

### Помилки

**`DOM_INVALID_CHARACTER_ERR`**

Виникає, якщо `target` містить неприпустимі символи.

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
-   [DOMDocument::createTextNode()](domdocument.createtextnode.html) - Створити новий текстовий вузол