Оголошує атрибут, вказаний вузлом, з ідентифікатором типу

-   [« DOMElement::setIdAttribute](domelement.setidattribute.html)
    
-   [DOMElement::setIdAttributeNS »](domelement.setidattributens.html)
    
-   [PHP Manual](index.html)
    
-   [DOMElement](class.domelement.html)
    
-   Оголошує атрибут, вказаний вузлом, з ідентифікатором типу
    

# DOMElement::setIdAttributeNode

(PHP 5, PHP 7, PHP 8)

DOMElement::setIdAttributeNode — Оголошує атрибут, вказаний вузлом, з ідентифікатором типу

### Опис

```methodsynopsis
public DOMElement::setIdAttributeNode(DOMAttr $attr, bool $isId): void
```

Оголошує атрибут, який визначається вузлом `attr`, ідентифікатор типу.

### Список параметрів

`attr`

Вузол атрибуту.

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
-   [DOMElement::setIdAttributeNS()](domelement.setidattributens.html) - Оголошує атрибут, вказаний локальним ім'ям та URI простору імен, з ідентифікатором типу