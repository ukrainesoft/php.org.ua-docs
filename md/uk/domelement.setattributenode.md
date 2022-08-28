Додає новий вузол атрибуту елемент

-   [« DOMElement::setAttribute](domelement.setattribute.html)
    
-   [DOMElement::setAttributeNodeNS »](domelement.setattributenodens.html)
    
-   [PHP Manual](index.html)
    
-   [DOMElement](class.domelement.html)
    
-   Додає новий вузол атрибуту елемент
    

# DOMElement::setAttributeNode

(PHP 5, PHP 7, PHP 8)

DOMElement::setAttributeNode — Додає новий вузол атрибута до елементу

### Опис

```methodsynopsis
public DOMElement::setAttributeNode(DOMAttr $attr): DOMAttr|null|false
```

Додає новий вузол атрибуту `attr` елемент.

### Список параметрів

`attr`

Вузол атрибуту.

### Значення, що повертаються

Повертає старий вузол, якщо атрибут замінено або **`null`**

### Помилки

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**

Виникає, якщо вузол доступний лише читання.

### Дивіться також

-   [DOMElement::hasAttribute()](domelement.hasattribute.html) - Перевіряє, чи існує атрибут
-   [DOMElement::getAttributeNode()](domelement.getattributenode.html) - Повертає вузол атрибуту
-   [DOMElement::removeAttributeNode()](domelement.removeattributenode.html) - Видаляє атрибут