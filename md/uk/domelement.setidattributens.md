Оголошує атрибут, вказаний локальним ім'ям та URI простору імен, з ідентифікатором типу

-   [« DOMElement::setIdAttributeNode](domelement.setidattributenode.html)
    
-   [DOMEntity »](class.domentity.html)
    
-   [PHP Manual](index.html)
    
-   [DOMElement](class.domelement.html)
    
-   Оголошує атрибут, вказаний локальним ім'ям та URI простору імен, з ідентифікатором типу
    

# DOMElement::setIdAttributeNS

(PHP 5, PHP 7, PHP 8)

DOMElement::setIdAttributeNS — Оголошує атрибут, вказаний локальним ім'ям та URI простору імен, з ідентифікатором типу

### Опис

```methodsynopsis
public DOMElement::setIdAttributeNS(string $namespace, string $qualifiedName, bool $isId): void
```

Оголошує атрибут, вказаний локальним іменем `qualifiedName` та простором імен `namespace`, ідентифікатор типу.

### Список параметрів

`namespace`

URI простір імен атрибута.

`qualifiedName`

Локальне ім'я атрибута у вигляді `prefix:tagname`

`isId`

Встановіть значення в **`true`** якщо ви хочете, щоб `name` мав ідентифікатор типу, **`false`** в іншому випадку.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**

Виникає, якщо вузол доступний лише читання.

**`DOM_NOT_FOUND`**

Виникає, якщо `name` не є атрибутом елемента.

### Дивіться також

-   [DOMDocument::getElementById()](domdocument.getelementbyid.html) - Шукає елемент із певним ідентифікатором
-   [DOMElement::setIdAttribute()](domelement.setidattribute.html) - Оголошує атрибут, вказаний ім'ям, з ідентифікатором типу
-   [DOMElement::setIdAttributeNode()](domelement.setidattributenode.html) - Оголошує атрибут, вказаний вузлом, з ідентифікатором типу