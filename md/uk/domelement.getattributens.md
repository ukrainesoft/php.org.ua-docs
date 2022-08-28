Повертає значення атрибуту

-   [« DOMElement::getAttributeNodeNS](domelement.getattributenodens.html)
    
-   [DOMElement::getElementsByTagName »](domelement.getelementsbytagname.html)
    
-   [PHP Manual](index.html)
    
-   [DOMElement](class.domelement.html)
    
-   Повертає значення атрибуту
    

# DOMElement::getAttributeNS

(PHP 5, PHP 7, PHP 8)

DOMElement::getAttributeNS — Повертає значення атрибуту

### Опис

```methodsynopsis
public DOMElement::getAttributeNS(?string $namespace, string $localName): string
```

Отримує значення атрибута у просторі імен `namespace` з локальним ім'ям `localName` для поточного сайту.

### Список параметрів

`namespace`

URI простір імен.

`localName`

Місцеве ім'я.

### Значення, що повертаються

Значення атрибуту або порожній рядок, якщо атрибут із заданим локальним ім'ям `localName` у просторі імен `namespace` НЕ знайдений.

### Дивіться також

-   [DOMElement::hasAttributeNS()](domelement.hasattributens.html) - Перевіряє, чи існує заданий атрибут
-   [DOMElement::setAttributeNS()](domelement.setattributens.html) - Додає новий атрибут
-   [DOMElement::removeAttributeNS()](domelement.removeattributens.html) - Видаляє атрибут