Додає новий атрибут елемент

-   [« DOMElement::setAttributeNode](domelement.setattributenode.md)
    
-   [DOMElement::setAttributeNS »](domelement.setattributens.md)
    
-   [PHP Manual](index.md)
    
-   [DOMElement](class.domelement.md)
    
-   Додає новий атрибут елемент
    

# DOMElement::setAttributeNodeNS

(PHP 5, PHP 7, PHP 8)

DOMElement::setAttributeNodeNS — Додає новий атрибут елемент

### Опис

```methodsynopsis
public DOMElement::setAttributeNodeNS(DOMAttr $attr): DOMAttr|null|false
```

Додає новий вузол атрибуту `attr` елемент.

### Список параметрів

`attr`

Вузол атрибуту.

### Значення, що повертаються

Повертає старий вузол, якщо атрибут замінено.

### Помилки

**`DOM_NO_MODIFICATION_ALLOWED_ERR`**

Виникає, якщо вузол доступний лише читання.

### Дивіться також

-   [DOMElement::hasAttributeNS()](domelement.hasattributens.md) - Перевіряє, чи існує заданий атрибут
-   [DOMElement::getAttributeNodeNS()](domelement.getattributenodens.md) - Повертає вузол атрибуту
-   [DOMElement::removeAttributeNode()](domelement.removeattributenode.md) - Видаляє атрибут