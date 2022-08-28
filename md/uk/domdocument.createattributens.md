Створює новий атрибут вузла з відповідним простором імен

-   [« DOMDocument::createAttribute](domdocument.createattribute.html)
    
-   [DOMDocument::createCDATASection »](domdocument.createcdatasection.html)
    
-   [PHP Manual](index.html)
    
-   [DOMDocument](class.domdocument.html)
    
-   Створює новий атрибут вузла з відповідним простором імен
    

# DOMDocument::createAttributeNS

(PHP 5, PHP 7, PHP 8)

DOMDocument::createAttributeNS — Створює новий атрибут вузла з відповідним простором імен

### Опис

```methodsynopsis
public DOMDocument::createAttributeNS(?string $namespace, string $qualifiedName): DOMAttr|false
```

Ця функція створює новий об'єкт класу [DOMAttr](class.domattr.html). Цей вузол не відображатиметься в документі, доки він не буде вставлений, наприклад, функцією [DOMNode::appendChild()](domnode.appendchild.html)

### Список параметрів

`namespace`

URI простір імен.

`qualifiedName`

Ім'я та префікс атрибуту у вигляді `prefix:tagname`

### Значення, що повертаються

Новий екземпляр класу [DOMAttr](class.domattr.html) або **`false`** у разі помилки.

### Помилки

**`DOM_INVALID_CHARACTER_ERR`**

Виникає, якщо `qualifiedName` містить неприпустимі символи.

**`DOM_NAMESPACE_ERR`**

Виникає, якщо `qualifiedName` неправильно сформовано, або якщо `qualifiedName` має префікс, а `namespace` має значення **`null`**

### Дивіться також

-   [DOMNode::appendChild()](domnode.appendchild.html) - Додає новий дочірній вузол до кінця списку нащадків
-   [DOMDocument::createAttribute()](domdocument.createattribute.html) - Створити новий атрибут
-   [DOMDocument::createCDATASection()](domdocument.createcdatasection.html) - Створює новий вузол cdata
-   [DOMDocument::createComment()](domdocument.createcomment.html) - Створити новий вузол коментаря
-   [DOMDocument::createDocumentFragment()](domdocument.createdocumentfragment.html) - створити новий фрагмент документа
-   [DOMDocument::createElement()](domdocument.createelement.html) - Створити новий вузол елемента
-   [DOMDocument::createElementNS()](domdocument.createelementns.html) - Створити новий вузол елемента з відповідним простором імен
-   [DOMDocument::createEntityReference()](domdocument.createentityreference.html) - Створити новий вузол посилання на суть
-   [DOMDocument::createProcessingInstruction()](domdocument.createprocessinginstruction.html) - Створити новий PI-вузол
-   [DOMDocument::createTextNode()](domdocument.createtextnode.html) - Створити новий текстовий вузол