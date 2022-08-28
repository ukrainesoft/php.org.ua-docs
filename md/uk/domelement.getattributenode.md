Повертає вузол атрибуту

-   [« DOMElement::getAttribute](domelement.getattribute.html)
    
-   [DOMElement::getAttributeNodeNS »](domelement.getattributenodens.html)
    
-   [PHP Manual](index.html)
    
-   [DOMElement](class.domelement.html)
    
-   Повертає вузол атрибуту
    

# DOMElement::getAttributeNode

(PHP 5, PHP 7, PHP 8)

DOMElement::getAttributeNode — Повертає вузол атрибуту

### Опис

```methodsynopsis
public DOMElement::getAttributeNode(string $qualifiedName): DOMAttr|DOMNameSpaceNode|false
```

Повертає вузол атрибута з ім'ям `qualifiedName` поточного елемента.

### Список параметрів

`qualifiedName`

Ім'я атрибуту.

### Значення, що повертаються

Вузол атрибуту. Зверніть увагу, що для об'яв просторів імен XML (атрибути `xmlns` і `xmlns:*`) повертається екземпляр **DOMNameSpaceNode**, а не [DOMAttr](class.domattr.html)

### Дивіться також

-   [DOMElement::hasAttribute()](domelement.hasattribute.html) - Перевіряє, чи існує атрибут
-   [DOMElement::setAttributeNode()](domelement.setattributenode.html) - Додає новий вузол атрибуту елемент
-   [DOMElement::removeAttributeNode()](domelement.removeattributenode.html) - Видаляє атрибут