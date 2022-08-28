Створити новий вузол посилання на суть

-   [« DOMDocument::createElementNS](domdocument.createelementns.html)
    
-   [DOMDocument::createProcessingInstruction »](domdocument.createprocessinginstruction.html)
    
-   [PHP Manual](index.html)
    
-   [DOMDocument](class.domdocument.html)
    
-   Створити новий вузол посилання на суть
    

# DOMDocument::createEntityReference

(PHP 5, PHP 7, PHP 8)

DOMDocument::create Entity Reference — Створити новий вузол посилання на суть

### Опис

```methodsynopsis
public DOMDocument::createEntityReference(string $name): DOMEntityReference|false
```

Ця функція створює екземпляр класу [DOMEntityReference](class.domentityreference.html). Цей вузол не буде відображатися в документі, доки він не буде вставлений, наприклад, функцією [DOMNode::appendChild()](domnode.appendchild.html)

### Список параметрів

`name`

Вміст посилання на сутність, наприклад, посилання на сутність без `&` на початку та `;` в кінці.

### Значення, що повертаються

Новий об'єкт класу [DOMEntityReference](class.domentityreference.html) або **`false`** у разі виникнення помилки.

### Помилки

**`DOM_INVALID_CHARACTER_ERR`**

Виникає, якщо `name` містить неприпустимі символи.

### Дивіться також

-   [DOMNode::appendChild()](domnode.appendchild.html) - Додає новий дочірній вузол до кінця списку нащадків
-   [DOMDocument::createAttribute()](domdocument.createattribute.html) - Створити новий атрибут
-   [DOMDocument::createAttributeNS()](domdocument.createattributens.html) - Створює новий атрибут вузла з відповідним простором імен
-   [DOMDocument::createCDATASection()](domdocument.createcdatasection.html) - Створює новий вузол cdata
-   [DOMDocument::createComment()](domdocument.createcomment.html) - Створити новий вузол коментаря
-   [DOMDocument::createDocumentFragment()](domdocument.createdocumentfragment.html) - створити новий фрагмент документа
-   [DOMDocument::createElement()](domdocument.createelement.html) - Створити новий вузол елемента
-   [DOMDocument::createElementNS()](domdocument.createelementns.html) - Створити новий вузол елемента з відповідним простором імен
-   [DOMDocument::createProcessingInstruction()](domdocument.createprocessinginstruction.html) - Створити новий PI-вузол
-   [DOMDocument::createTextNode()](domdocument.createtextnode.html) - Створити новий текстовий вузол