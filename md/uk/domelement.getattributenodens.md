Повертає вузол атрибуту

-   [« DOMElement::getAttributeNode](domelement.getattributenode.html)
    
-   [DOMElement::getAttributeNS »](domelement.getattributens.html)
    
-   [PHP Manual](index.html)
    
-   [DOMElement](class.domelement.html)
    
-   Повертає вузол атрибуту
    

# DOMElement::getAttributeNodeNS

(PHP 5, PHP 7, PHP 8)

DOMElement::getAttributeNodeNS — Повертає вузол атрибуту

### Опис

```methodsynopsis
public DOMElement::getAttributeNodeNS(?string $namespace, string $localName): DOMAttr|DOMNameSpaceNode|null
```

Повертає вузол атрибута у просторі імен `namespace` з локальним ім'ям `localName` для поточного сайту.

### Список параметрів

`namespace`

URI простір імен.

`localName`

Місцеве ім'я.

### Значення, що повертаються

Вузол атрибуту. Зверніть увагу, що для оголошень просторів імен XML (атрибути `xmlns` і `xmlns:*`) повертається екземпляр **DOMNameSpaceNode**, а не об'єкт [DOMAttr](class.domattr.html)

### Дивіться також

-   [DOMElement::hasAttributeNS()](domelement.hasattributens.html) - Перевіряє, чи існує заданий атрибут
-   [DOMElement::setAttributeNodeNS()](domelement.setattributenodens.html) - Додає новий атрибут елемент
-   [DOMElement::removeAttributeNode()](domelement.removeattributenode.html) - Видаляє атрибут